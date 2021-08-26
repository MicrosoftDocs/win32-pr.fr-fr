---
description: Cette rubrique fournit des conseils pour les développeurs sur la façon d’optimiser les performances et l’efficacité dans la pile de présentation sur les versions modernes de Windows.
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: Pour des performances optimales, utilisez DXGI Flip Model
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: ce999bc735042132902158cfd6bd6d41296d29a3afc98ab27d9480dc6bd8b3b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951219"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>Pour des performances optimales, utilisez DXGI Flip Model

Cette rubrique fournit des conseils pour les développeurs sur la façon d’optimiser les performances et l’efficacité dans la pile de présentation sur les versions modernes de Windows. il reprend là où [DXGI flip model](dxgi-flip-model.md), [DirectX 12 : Modes de présentation dans Windows 10 (vidéo)](https://www.youtube.com/watch?v=E3wTajGZOsA)et les [améliorations apportées à la présentation dans Windows 10 : l’apparence initiale (vidéo)](https://www.youtube.com/watch?v=nUZVV_mssWQ) s’est arrêtée.

## <a name="call-to-action"></a>Appel à l’action

Si vous utilisez toujours l’effet d' **\_ échange dxgi \_ \_ Discard ignore** ou **dxgi \_ swap \_ Effect \_ Sequential** (également appelé le modèle de présentation « BLT »), il est temps de s’arrêter !

Basculer vers l' **effet d’échange dxgi retourner l’effet de permutation \_ \_ \_ \_ séquentielle** ou d' **\_ échange dxgi \_ \_ Flip \_ ignore** (également appelé le modèle de retournement) offrira de meilleures performances, une consommation d’énergie plus faible et fournira un ensemble plus riche de fonctionnalités. (Pour plus d’informations sur ces valeurs, consultez [ \_ \_ énumération de l’effet d’échange dxgi](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) .)

L’outil retournement du modèle permet de faire en sorte que le mode fenêtre soit équivalent ou mieux comparé au mode « plein écran » classique. En fait, vous souhaiterez peut-être reconsidérer si votre application a réellement besoin d’un mode plein écran plein écran, car les avantages d’une fenêtre de basculement de modèle sans bordure incluent plus rapidement la Alt-Tab et une meilleure intégration avec les fonctionnalités d’affichage modernes.

Pourquoi maintenant ? Avant la mise à jour du 2018 d’avril, le modèle BLT présente un risque de destruction visible lorsqu’il est utilisé sur des configurations GPU hybrides, souvent détectées dans des ordinateurs portables haut de gamme (voir [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)). Dans la mise à jour d’avril 2018, ce déchirement a été corrigé, au détriment d’un travail supplémentaire. Si vous utilisez BLT à des trames élevés sur des GPU hybrides, en particulier pour des résolutions élevées comme 4 Ko, ce travail supplémentaire peut affecter les performances globales. Pour garantir des performances optimales sur ces systèmes, passez du BLT au modèle de basculement. En outre, envisagez de réduire la résolution de vos utilise permutation, surtout s’il ne s’agit pas du point principal de l’interaction utilisateur (comme c’est souvent le cas avec les fenêtres en version préliminaire de VR).

## <a name="a-brief-history"></a>Bref historique

Qu’est-ce que le modèle de basculement ? Qu’est-ce que l’alternative ?

avant le Windows 7, le seul moyen de présenter le contenu à partir de D3D était de « blt » ou de le copier dans une surface qui était la propriété de la fenêtre ou de l’écran. à partir de D3D9's FLIPEX swap effect et à DXGI via l' \_ effet de permutation séquentielle dans Windows 8, nous avons développé un moyen plus efficace de placer du contenu sur l’écran en le partageant directement avec le compositeur de bureau, avec des copies minimales. Pour une vue d’ensemble globale de la technologie, consultez [dxgi Flip Model](dxgi-flip-model.md) .

cette optimisation est possible grâce au DWM (Gestionnaire de fenêtrage), qui est le compositeur qui pilote le bureau Windows.

## <a name="when-should-i-use-the-blt-model"></a>Quand dois-je utiliser le modèle BLT ?

Le modèle de retournement ne fournit qu’une partie des fonctionnalités : la possibilité d’avoir plusieurs API différentes produisant du contenu, qui se trouvent toutes les couches dans le même **HWND**, sur une base actuelle. c’est le cas, par exemple, si vous utilisez D3D pour dessiner un arrière-plan de fenêtre, puis [Windows GDI](/windows/desktop/gdi/windows-gdi) pour dessiner des éléments en haut, ou à l’aide de deux api graphiques différentes, ou de deux chaînes d’échange à partir de la même api, pour produire des images alternées. Si vous n’avez pas besoin d’une interopérabilité au niveau **HWND** entre les composants Graphics, vous n’avez pas besoin d’un modèle BLT.

Il existe une deuxième partie des fonctionnalités qui n’a pas été fournie dans la conception du modèle de retournement d’origine, mais qui est désormais disponible, ce qui est la possibilité de présenter une cadence non limitée. Pour une application utilisant l’intervalle de synchronisation 0, nous vous déconseillons de passer à l’option Inverser le modèle, sauf si l’API [IDXGIFactory5 :: CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) est disponible et que les rapports sur la prise en charge de la **\_ fonctionnalité dxgi peuvent être \_ \_ \_ détruits**. cette fonctionnalité est presque omniprésente dans les versions récentes de Windows 10 et sur le matériel moderne.

## <a name="directflip"></a>DirectFlip

si vous avez regardé [DirectX 12 : Modes de présentation dans Windows 10](https://www.youtube.com/watch?v=E3wTajGZOsA), vous verrez des informations sur les « retournements directs » et les « retournements indépendants ». Il s’agit d’optimisations activées pour les applications à l’aide de l’option Flip Model chaînes d’échange. En fonction de la configuration de la fenêtre et de la mémoire tampon, il est possible de contourner entièrement la composition du bureau et d’envoyer directement des frames d’application à l’écran, de la même façon que le mode plein écran exclusif.

Ces optimisations peuvent être menées dans l’un des trois scénarios, dans l’ordre des fonctionnalités les plus nombreuses :

1.  **DirectFlip**: vos mémoires tampons utilise permutation correspondent aux dimensions de l’écran, et la région de votre client Windows couvre l’écran. Au lieu d’utiliser le DWM utilise permutation à afficher à l’écran, l’application utilise permutation est utilisée.
2.  **DirectFlip avec les installateurs de panneau**: la région de votre client Windows couvre l’écran et vos tampons utilise permutation se trouvent dans un facteur d’échelle dépendant du matériel (par exemple, 0,25 x à 4 fois) de l’écran. Le matériel scanout GPU est utilisé pour mettre à l’échelle votre mémoire tampon lors de son envoi à l’affichage.
3.  **DirectFlip avec multi-plan overlay (MPO)**: vos mémoires tampons utilise permutation se trouvent dans un facteur d’échelle dépendant du matériel de vos dimensions de fenêtre. Le DWM est en mesure de réserver un plan de scanout matériel dédié à votre application, qui est ensuite analysé et éventuellement étiré sur une sous-région à contrôle alpha de l’écran.

Avec le modèle de retournement à fenêtres, l’application peut interroger la prise en charge matérielle pour différents scénarios de DirectFlip et implémenter différents types de mise à l’échelle dynamique à l’aide de [IDXGIOutput6 :: CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport). Gardez à l’esprit que si les installateurs de volet sont utilisés, il est possible que le curseur subisse des effets secondaires d’étirement, ce qui est indiqué par le biais de la **\_ composition matérielle dxgi \_ \_ prise en charge \_ \_ \_** de la composition du curseur.

Une fois que votre utilise permutation a été « DirectFlipped », le DWM peut passer en mode veille et se réveiller uniquement en cas de changement en dehors de votre application. Les frames de votre application sont envoyés directement à l’écran, de manière indépendante, avec la même efficacité que le mode plein écran. Il s’agit d’un « inverseur indépendant » qui peut s’impliquer dans tous les scénarios ci-dessus. Si le contenu d’un autre bureau est en haut, le DWM peut passer en toute transparence en mode composé, « inverser la composition » de manière efficace et le contenu en haut de l’application avant de le retourner, ou tirer parti de MPO pour maintenir le mode de retournement indépendant.

Consultez l’outil [PresentMon](https://github.com/GameTechDev/PresentMon) pour obtenir des informations sur les éléments qui ont été utilisés.

## <a name="what-else-is-new-in-the-flip-model"></a>Quelles sont les autres nouveautés du modèle de basculement ?

En plus des améliorations apportées ci-dessus, qui s’appliquent aux chaînes d’échange standard sans rien de spécial, plusieurs fonctionnalités sont disponibles pour les applications de retournement à utiliser :

-   Latence décroissant à l’aide d’un **objet d' \_ indicateur de \_ \_ \_ \_ latence \_ \_ de trame de la chaîne d’échange dxgi**. en mode de basculement indépendant, vous pouvez atteindre 1 image de latence sur les versions récentes de Windows, avec un secours normal au minimum possible quand il est composé.
    -   inconvénient : nous avons rencontré un problème qui a donné un minimum de deux trames de latence dans la Windows 10 mise à jour anniversaire et versions antérieures. Pour plus d’informations, consultez [ce forum](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) . Ce problème est résolu dans la mise à jour du créateur de l’automne.
-   **Dxgi \_ Permuter l' \_ effet \_ Flip \_ ignore** active le mode de « composition inversée » d’un retournement direct, ce qui entraîne moins de travail global pour l’affichage du bureau. Le DWM peut faire un griffonnage sur les mémoires tampons de l’application et les envoyer à l’écran, au lieu d’effectuer une copie complète dans son propre chaînes d’échange.
-   **Dxgi \_ L' \_ indicateur de chaîne de \_ \_ \_ permutation** peut permettre une latence encore inférieure à celle de l’objet pouvant être attendu, même dans une fenêtre sur les systèmes avec prise en charge de la superposition à plusieurs plans.
-   Les applications contrôlent la mise à l’échelle du contenu qui se produit pendant le redimensionnement de la fenêtre, à l’aide de la propriété de [ \_ mise à l’échelle dxgi](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) pendant la création de utilise permutation.
-   Le contenu des formats HDR (R10G10B10A2 \_ UNORM ou R16G16B16A16 \_ float) n’est pas ancré, sauf s’il est composé d’un ordinateur de bureau SDR.
-   Les statistiques sont disponibles en mode fenêtre.
-   il existe une plus grande compatibilité avec le modèle d’application UWP (plateforme Windows universelle) et DX12, car ceux-ci sont uniquement compatibles avec le modèle de retournement.

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>Que dois-je faire pour utiliser le modèle de retournement ?

Flip Model chaînes d’échange présente quelques exigences supplémentaires en plus de la chaînes d’échange BLT :

1.  Le nombre de tampons doit être au moins égal à 2.
2.  Après [l’appel de](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) , la mémoire tampon d’arrière-plan doit être explicitement reliée au contexte immédiat d3d11 avant de pouvoir être réutilisée.
3.  Après l’appel de [SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate), l’application doit appeler [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) avant la **présente**.
4.  Les chaînes d’échange MSAA (MultiSample anti-aliasing) ne sont pas directement pris en charge dans le modèle de retournement. l’application devra donc effectuer une résolution MSAA avant d’émettre le **présent**.

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>Comment choisir le rendu approprié et les résolutions de présentation

Le modèle traditionnel pour les applications dans le passé a été de fournir à l’utilisateur une liste de résolutions à choisir lorsque l’utilisateur sélectionne le mode plein écran exclusif. Avec la capacité des affichages modernes à commencer à mettre à l’échelle le contenu en toute transparence, envisagez de fournir aux utilisateurs la possibilité de choisir une résolution de rendu pour la mise à l’échelle des performances, indépendamment d’une résolution de sortie et même en mode fenêtre. En outre, les applications doivent tirer parti de **IDXGIOutput6 :: CheckHardwareCompositionSupport** pour déterminer si elles doivent mettre à l’échelle le contenu avant de le présenter, ou si elles doivent permettre au matériel d’effectuer la mise à l’échelle.

Vous devrez peut-être migrer votre contenu d’un GPU vers un autre dans le cadre de l’opération de présentation ou de composition. C’est souvent le cas sur les ordinateurs portables à plusieurs GPU ou sur des systèmes avec des GPU externes branchés. Étant donné que ces configurations sont plus courantes et que les affichages haute résolution deviennent plus courants, le coût de la présentation d’un utilise permutation à résolution complète augmente. Si la cible de votre utilise permutation n’est pas le point principal de l’interaction de l’utilisateur, comme c’est souvent le cas avec des titres VR qui présentent une préversion 2D de la scène VR dans une fenêtre secondaire, envisagez d’utiliser une résolution inférieure utilise permutation pour réduire la quantité de bande passante qui doit être transférée entre les différentes GPU.

## <a name="other-considerations"></a>Autres éléments à prendre en compte

La première fois que vous demandez au GPU d’écrire dans la mémoire tampon d’arrière-plan utilise permutation est la durée pendant laquelle le GPU est bloqué en attendant que la mémoire tampon devienne disponible. Dans la mesure du possible, retardez ce point autant que possible dans le frame.

 

 
