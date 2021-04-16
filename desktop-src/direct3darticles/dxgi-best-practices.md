---
title: Méthodes recommandées pour l’infrastructure DirectX Graphics (DXGI)
description: Cet article aborde les principaux problèmes de Portage.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f576368674d05af74e3161d4251301ebc066a489
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382412"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX Graphics infrastructure (DXGI) : meilleures pratiques

Microsoft DirectX Graphics infrastructure (DXGI) est un nouveau sous-système qui a été introduit avec Windows Vista, qui encapsule certaines des tâches de bas niveau requises par Direct3D 10, 10,1, 11 et 11,1. Du point de vue d’un programmeur Direct3D 9, DXGI englobe la majeure partie du code pour l’énumération, la création de chaîne d’échange et la présentation précédemment compressées dans les API Direct3D 9. Lorsque vous portez une application sur DXGI et Direct3D 10. x et Direct3D 11. x, vous devez prendre en compte certaines considérations pour vous assurer que le processus s’exécute correctement.

Cet article aborde les principaux problèmes de Portage.

-   [Problèmes liés à l’écran complet](#full-screen-issues)
-   [Moniteurs multiples](#multiple-monitors)
-   [Styles de fenêtre et DXGI](#window-styles-and-dxgi)
-   [Multithread et DXGI](#multithreading-and-dxgi)
-   [Gamma et DXGI](#gamma-and-dxgi)
-   [DXGI 1,1](#dxgi-11)
-   [DXGI 1,2](#dxgi-12)

## <a name="full-screen-issues"></a>Problèmes de Full-Screen

Dans le portage de Direct3D 9 vers DXGI et vers Direct3D 10. x ou Direct3D 11. x, les problèmes liés au passage d’une fenêtre à l’autres en mode plein écran peuvent souvent provoquer des tracas pour les développeurs. Les principaux problèmes sont dus au fait que les applications Direct3D 9, contrairement aux applications DXGI, nécessitent une approche plus pratique pour suivre les styles de fenêtre et les États de fenêtre. Lorsque le code de modification en mode est porté pour s’exécuter sur DXGI, il provoque souvent un comportement inattendu.

Souvent, les applications Direct3D 9 géraient la transition en mode plein écran en définissant la résolution du tampon avant, en forçant l’appareil en mode exclusif plein écran, puis en définissant les résolutions de la mémoire tampon d’arrière-plan en conséquence. Un chemin d’accès distinct a été utilisé pour les modifications apportées à la taille de la fenêtre, car elles devaient être gérées à partir du processus de fenêtre chaque fois que l’application a reçu un \_ message de taille WM.

DXGI tente de simplifier cette approche en combinant les deux cas. Par exemple, lorsque vous faites glisser la bordure de la fenêtre en mode fenêtre, l’application reçoit un \_ message de taille WM. DXGI intercepte ce message et redimensionne automatiquement le tampon d’avant. L’application a uniquement besoin d’appeler [**IDXGISwapChain :: ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) pour redimensionner la mémoire tampon d’arrière-plan en fonction de la taille transmise en tant que paramètres dans la taille de WM \_ . De même, lorsque l’application doit basculer entre le mode plein écran et le mode fenêtre, l’application peut simplement appeler [**IDXGISwapChain :: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI redimensionne la mémoire tampon d’attente pour qu’elle corresponde au mode plein écran sélectionné et envoie un \_ message de taille WM à l’application. L’application appelle à nouveau **ResizeBuffers**, comme c’est le cas si la bordure de la fenêtre a été déplacée.

La méthodologie de l’explication précédente suit un chemin d’accès très particulier. DXGI définit la résolution de l’écran complet sur la résolution du bureau par défaut. De nombreuses applications, toutefois, basculent vers une résolution à l’écran par défaut. Dans ce cas, DXGI fournit [**IDXGISwapChain :: ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Cette méthode doit être appelée avant d’appeler [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). Bien que ces méthodes puissent être appelées dans l’ordre inverse (**SetFullscreenState** en premier, suivi par **ResizeTarget**), cela entraîne l’envoi d’un message de taille WM supplémentaire \_ à l’application. (Cela peut également provoquer un scintillement, car DXGI peut être forcé à effectuer deux modifications de mode.) Après l’appel de **SetFullscreenState**, il est recommandé d’appeler à nouveau **ResizeTarget** avec le membre **RefreshRate** du [**\_ mode dxgi \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) mis à zéro. Il s’agit d’une instruction de non-opération dans DXGI, mais elle peut éviter des problèmes liés à la fréquence d’actualisation, qui sont abordés ci-après.

En mode plein écran, le Gestionnaire de fenêtrage (DWM) est désactivé. DXGI peut effectuer un retournement pour présenter le contenu de la mémoire tampon d’arrière-plan au lieu d’effectuer un blit, ce qui serait le cas en mode fenêtre. Ce gain de performance peut cependant être annulé si certaines exigences ne sont pas satisfaites. Pour vous assurer que DXGI effectue un retournement au lieu d’un blit, le tampon d’avant et l’arrière-plan doivent être dimensionnés de façon identique. Si l’application gère correctement ses \_ messages de taille WM, cela ne doit pas être un problème. En outre, les formats doivent être identiques.

Le problème pour la plupart des applications est la fréquence d’actualisation. La fréquence d’actualisation spécifiée dans l’appel à [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) doit être un taux d’actualisation qui est énuméré par l’objet [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que la chaîne de permutation utilise. DXGI peut calculer automatiquement cette valeur si l’application revient au membre **RefreshRate** du [**\_ mode dxgi \_ desc**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) passé dans **ResizeTarget**. Il est important de ne pas supposer que certains taux d’actualisation seront toujours pris en charge et de coder en dur une valeur. Souvent, les développeurs choisissent 60 Hz comme taux d’actualisation, sans savoir que le taux d’actualisation énuméré du moniteur est approximativement de 60 000/1 001 Hz à partir du moniteur. Si la fréquence d’actualisation ne correspond pas au taux d’actualisation attendu de 60, DXGI est forcé d’effectuer un blit en mode plein écran au lieu d’un retournement.

Le dernier problème que rencontrent souvent les développeurs est la modification des résolutions en plein écran, tout en restant en mode plein écran. L’appel de [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) et de [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) peut parfois aboutir, mais la résolution plein écran reste la résolution du bureau. En outre, les développeurs peuvent créer une chaîne d’échange plein écran et fournir une résolution spécifique, uniquement pour déterminer que DXGI a comme valeur par défaut la résolution du bureau, quels que soient les nombres transmis. Sauf instruction contraire, DXGI est défini par défaut sur la résolution du Bureau pour les chaînes d’échange plein écran. Lors de la création d’une chaîne de permutation plein écran, le membre **Flags** de la structure DESC de la [**\_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) doit être défini sur le [**\_ \_ \_ \_ \_ \_ basculement du mode allow**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) de la chaîne de permutation DXGI pour remplacer le comportement par défaut de DXGI. Cet indicateur peut également être passé à **ResizeTarget** pour activer ou désactiver cette fonctionnalité de manière dynamique.

## <a name="multiple-monitors"></a>Moniteurs multiples

Lorsque vous utilisez DXGI avec plusieurs moniteurs, vous pouvez suivre deux règles.

La première règle s’applique à la création d’au moins deux chaînes d’échange plein écran sur plusieurs moniteurs. Lors de la création de chaînes de permutation, il est préférable de créer toutes les chaînes de permutation sous forme de fenêtre, puis de les définir en plein écran. Si les chaînes d’échange sont créées en mode plein écran, la création d’une deuxième chaîne de permutation entraîne l’envoi d’une modification de mode à la première chaîne de permutation, ce qui peut entraîner l’arrêt du mode plein écran.

La deuxième règle s’applique aux sorties. Watchful des sorties utilisées lors de la création de chaînes de permutation. Avec DXGI, l’objet [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) contrôle l’analyse que la chaîne de permutation utilise en mode plein écran. Contrairement à DXGI, Direct3D 9 n’avait aucun concept de sorties.

## <a name="window-styles-and-dxgi"></a>Styles de fenêtre et DXGI

Les applications Direct3D 9 ont beaucoup de travail à effectuer lors du basculement entre les modes plein écran et fenêtre. Une grande partie de ce travail impliquait de modifier les styles de fenêtre pour ajouter et supprimer des bordures, pour ajouter des barres de défilement, et ainsi de suite. Lorsque les applications sont portées dans DXGI et Direct3D 10. x ou Direct3D 11. x, ce code est souvent laissé en place. En fonction des modifications apportées, le basculement entre les modes peut entraîner un comportement inattendu. Par exemple, lorsque vous passez en mode fenêtre, l’application peut ne plus avoir de cadre de fenêtre ou de bordure de fenêtre malgré le fait que le code définisse spécifiquement ces styles. Cela est dû au fait que DXGI gère à présent une grande partie de ce style qui change de manière autonome. La définition manuelle des styles de fenêtre peut interférer avec DXGI, ce qui peut provoquer un comportement inattendu.

Le comportement recommandé consiste à effectuer le moins de travail possible et à laisser DXGI gérer la majeure partie de l’interaction avec les fenêtres. Toutefois, si l’application doit gérer son propre comportement de fenêtrage, [**IDXGIFactory :: MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) peut être utilisé pour indiquer à dxgi de désactiver une partie de sa gestion automatique de fenêtre.

## <a name="multithreading-and-dxgi"></a>Multithread et DXGI

Une attention particulière doit être prise lors de l’utilisation de DXGI dans une application multithread pour s’assurer que les blocages ne se produisent pas. En raison de l’interaction étroite de DXGI avec la fenêtrage, il envoie parfois des messages de fenêtre à la fenêtre d’application associée. DXGI a besoin que les modifications de fenêtrage se produisent avant de pouvoir continuer. il utilisera donc [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), qui est un appel synchrone. L’application doit traiter le message de fenêtre avant que **SendMessage** retourne.

Dans une application où les appels DXGI et la pompe de messages se trouvent sur le même thread (ou une application à thread unique), peu de choses doivent être effectuées. Lorsque l’appel DXGI se trouve sur le même thread que la pompe de messages, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) appelle la fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))de la fenêtre. Cela contourne la pompe de messages et permet à l’exécution de continuer après l’appel à **SendMessage**. N’oubliez pas que les appels [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) , tels que [**IDXGISwapChain ::P renvoyés**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), sont également considérés comme des appels DXGI. DXGI peut différer le travail de [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) ou [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) jusqu’à ce que le **présent** soit appelé.

Si l’appel DXGI et la pompe de messages se trouvent sur des threads différents, vous devez veiller à éviter les interblocages. Lorsque la pompe de messages et SendMessage se trouvent sur des threads différents, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ajoute un message à la file d’attente de messages de la fenêtre et attend que la fenêtre traite ce message. Si la procédure de fenêtre est occupée ou n’est pas appelée par la pompe de messages, le message peut ne jamais être traité et DXGI attend indéfiniment.

Par exemple, si une application qui a sa pompe de messages sur un thread et son rendu sur un autre, il peut être utile de modifier les modes. Le thread de pompe de messages indique au thread de rendu de modifier les modes et attend la fin du changement de mode. Toutefois, le thread de rendu appelle les fonctions DXGI, qui à leur tour appellent [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), qui se bloque jusqu’à ce que la pompe de messages traite le message. Un blocage se produit parce que les deux threads sont désormais bloqués et attendent les uns les autres. Pour éviter cela, ne bloquez jamais la pompe de messages. Si un bloc est inévitable, toutes les interactions DXGI doivent se produire sur le même thread que la pompe de messages.

## <a name="gamma-and-dxgi"></a>Gamma et DXGI

Bien que gamma puisse être mieux géré dans Direct3D 10. x ou Direct3D 11. x en utilisant des textures sRVB, la rampe gamma peut toujours être utile pour les développeurs qui souhaitent une valeur gamma différente de 2,2 ou qui utilisent un format de cible de rendu qui ne prend pas en charge SRGB. Tenez compte de deux problèmes lors de la définition de la rampe gamma par le biais de DXGI. Le premier problème est que les valeurs de rampe passées dans [**IDXGIOutput :: SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) sont des valeurs float, et non des valeurs de **mot** . En outre, assurez-vous que le code porté à partir de Direct3D 9 ne tente pas de convertir en valeurs **Word** avant de les passer à **SetGammaControl**.

Le deuxième problème est que, après avoir changé en mode plein écran, [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) peut ne pas sembler fonctionner, en fonction de l’objet [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) utilisé. Lors du passage en mode plein écran, DXGI crée un nouvel objet de sortie et utilise l’objet pour toutes les opérations suivantes sur la sortie. Si vous appelez **SetGammaControl** sur une sortie énumérée avant un commutateur en mode plein écran, l’appel n’est pas dirigé vers la sortie actuellement utilisée par DXGI. Pour éviter cela, appelez [**IDXGISwapChain :: GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) pour accéder à la sortie actuelle, puis appelez **SetGammaControl** à partir de cette sortie pour connaître le comportement correct.

Pour plus d’informations sur l’utilisation de la correction gamma, consultez Utilisation de la [correction gamma](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1,1

Le runtime Direct3D 11 inclus dans Windows 7 et installé sur Windows Vista (voir [KB971644](https://support.microsoft.com/kb/971644)) inclut la version 1,1 de DXGI. Cette mise à jour ajoute des définitions pour un certain nombre de nouveaux formats (notamment BGRA, le biais de 10 bits x2 et la compression de texture BC6H et BC7 de Direct3D 11), ainsi qu’une nouvelle version de la fabrique DXGI et des interfaces d’adaptateur ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) pour l’énumération des connexions Bureau à distance.

Lorsque vous utilisez Direct3D 11, le runtime utilise DXGI 1,1 par défaut lors de l’appel de [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) avec un pointeur [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) null. Le mélange de l’utilisation de DXGI 1,0 et de DXGI 1,1 dans le même processus n’est pas pris en charge. La combinaison d’instances d’objet DXGI de différentes fabriques dans le même processus n’est pas prise en charge. Par conséquent, lorsque vous utilisez DirectX 11, toute utilisation explicite des interfaces DXGI utilise un [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) créé par le point d’entrée [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) dans « DXGI.DLL » pour s’assurer que l’application utilise toujours DXGI 1,1.

## <a name="dxgi-12"></a>DXGI 1,2

Le runtime Direct3D 11,1 inclus dans Windows 8 inclut également la version 1,2 de DXGI.

DXGI 1,2 active les fonctionnalités suivantes :

-   rendu stéréo
-   formats 16 bits par pixel

    -   Les formats DXGI \_ \_ B5G6R5 \_ UNORM et \_ dxgi \_ B5G5R5A1 \_ UNORM sont désormais entièrement pris en charge
    -   un nouveau \_ format dxgi \_ B5G5R5A1 \_ UNORM a été ajouté

-   formats vidéo
-   nouvelles interfaces DXGI

Pour plus d’informations sur les fonctionnalités de DXGI 1,2, consultez [améliorations apportées à DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 