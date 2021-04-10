---
description: Windows 8 ajoute la prise en charge du modèle de retournement de présentation et de ses statistiques actuelles associées dans DXGI 1,2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: DXGI Flip Model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846405"
---
# <a name="dxgi-flip-model"></a>DXGI Flip Model

Windows 8 ajoute la prise en charge du modèle de retournement de présentation et de ses statistiques actuelles associées dans DXGI 1,2. Le modèle de retournement de DXGI de Windows 8 est similaire à la [Présentation du mode de basculement Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md)de Windows 7. Les applications de présentation basées sur la fréquence d’images ou la vidéo, comme les jeux, peuvent tirer le meilleur parti en utilisant le modèle de retournement de présentation. Les applications qui utilisent DXGI retournent le modèle de présentation réduisent la charge des ressources système et améliorent les performances. Les applications peuvent également utiliser l’amélioration de la présentation des statistiques avec la fonction retourner le modèle de présentation pour mieux contrôler le taux de présentation en fournissant des mécanismes de commentaires et de correction en temps réel.

-   [Comparaison du modèle de retournement DXGI et du modèle BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Guide pratique pour utiliser DXGI Flip Model](#how-to-use-dxgi-flip-model)
-   [Synchronisation des frames des applications DXGI Flip Model](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Prévention, détection et récupération à partir de problèmes](#avoiding-detecting-and-recovering-from-glitches)
-   [Rubriques connexes](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Comparaison du modèle de retournement DXGI et du modèle BitBlt

Le runtime utilise le transfert de bloc de bits (BitBlt) et retournent les modèles de présentation pour présenter le contenu graphique sur les moniteurs d’affichage. La plus grande différence entre BitBlt et retourner les modèles de présentation est la façon dont le contenu de la mémoire tampon d’arrière-plan est obtenu dans le DWM Windows 8 pour la composition. Dans le modèle BitBlt, le contenu de la mémoire tampon d’arrière-plan est copié dans la surface de redirection de chaque appel à [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Dans le modèle de retournement, toutes les mémoires tampons d’arrière-plan sont partagées avec le Gestionnaire de fenêtrage (DWM). Par conséquent, le DWM peut composer directement à partir de ces mémoires tampons d’arrière-plan sans aucune autre opération de copie. En général, le modèle de retournement est plus efficace. Le modèle de retournement fournit également plus de fonctionnalités, telles que les statistiques actuelles améliorées.

Si vous avez des composants hérités qui utilisent Windows Graphics Device Interface (GDI) pour écrire directement dans un [**HWND**](../winprog/windows-data-types.md) , utilisez le modèle BitBlt.

Les améliorations des performances du modèle de basculement DXGI sont significatives quand l’application est en mode fenêtre. La séquence de ce tableau et l’illustration comparent les utilisations de la bande passante de mémoire et les lectures et écritures système des applications Windows qui choisissent le modèle Flip Model et le modèle BitBlt.



| Étape | Modèle BitBlt présent dans DWM                                                                               | DXGI Flip Model est présent dans DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | L’application met à jour son Frame (écriture)<br/>                                                              | L’application met à jour son Frame (écriture)<br/>                     |
| 2.   | Le runtime Direct3D copie le contenu de la surface dans une surface de redirection DWM (lecture, écriture)<br/>            | Le runtime Direct3D passe l’aire de l’application à DWM<br/>        |
| 3.   | Une fois la copie de la surface partagée terminée, DWM restitue l’aire de l’application sur l’écran (lecture, écriture)<br/> | DWM affiche l’aire de l’application sur l’écran (lecture, écriture)<br/> |



 

![illustration d’une comparaison entre le modèle BLT et le modèle Flip](images/blt-flip-mode-present.png)

Flip Model réduit l’utilisation de la mémoire système en réduisant le nombre de lectures et d’écritures par le runtime Direct3D pour la composition de frame avec fenêtres par DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Guide pratique pour utiliser DXGI Flip Model

Les applications Direct3D 11,1 qui ciblent Windows 8 utilisent Flip Model en créant la chaîne de permutation avec l' [**effet d’échange dxgi retourner une valeur d’énumération \_ \_ \_ \_ séquentielle**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) définie dans le membre **SwapEffect** de la structure DESC1 de la [**\_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) . Quand vous définissez **SwapEffect** sur **dxgi \_ swap \_ Effect, \_ retournez \_ séquentiellement**, définissez également les membres de la **chaîne de \_ permutation dxgi \_ \_ DESC1** sur les valeurs indiquées :

-   **BufferCount** à une valeur comprise entre 2 et 16 pour empêcher une baisse des performances due à l’attente de la libération du tampon de présentation précédent par le DWM.
-   **Formatez** -le au format dxgi \_ \_ R16G16B16A16 \_ float, DXGI \_ format \_ B8G8R8A8 \_ UNORM ou dxgi R8G8B8A8 \_ \_ \_ UNORM
-   Membre **Count** de la structure dxgi de l' [**\_ exemple \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) que le membre **SampleDesc** spécifie à un et le membre **Quality** de **dxgi \_ exemple \_ desc** à zéro parce que le multiple Sample anticrénelage (MSAA) n’est pas pris en charge

Si vous utilisez [**l' \_ effet d’échange dxgi, \_ \_ retournez \_ séquentiellement**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) sur le système d’exploitation Windows 7 ou antérieur, la création de l’appareil échoue. Lorsque vous utilisez Flip Model, vous pouvez utiliser les statistiques de plein écran en mode fenêtre. Le comportement de plein écran n’est pas affecté. Si vous passez la **valeur null** au paramètre *pFullscreenDesc* de [**IDXGIFactory2 :: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) pour une chaîne de permutation avec fenêtres et que vous définissez **SwapEffect** sur **dxgi \_ swap \_ Effect \_ Flip \_ Sequential**, le runtime crée une mémoire tampon d’arrière-plan supplémentaire et fait pivoter le handle qui appartient à la mémoire tampon qui devient la mémoire tampon d’arrière-plan au moment de la présentation.

Quand vous utilisez Flip Model, tenez compte des conseils suivants :

-   Utilisez une chaîne de permutation de modèle par [**HWND**](../winprog/windows-data-types.md). Ne ciblez pas plusieurs chaînes de basculement de modèle vers le même **HWND**.
-   N’utilisez pas Flip Model swap Chain avec la fonction [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) ou [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) de GDI. Certaines applications Direct3D utilisent les fonctions **ScrollWindow** et **ScrollWindowEx** de GDI pour mettre à jour le contenu de la fenêtre après qu’un événement de défilement utilisateur s’est produit. **ScrollWindow** et **ScrollWindowEx** effectuent le bitblts du contenu des fenêtres à l’écran lorsque l’utilisateur fait défiler une fenêtre. Ces fonctions nécessitent également des mises à jour du modèle BitBlt pour le contenu GDI et Direct3D. Les applications qui utilisent l’une ou l’autre des fonctions n’affichent pas nécessairement le contenu visible des fenêtres à l’écran quand l’application est en mode fenêtre. Nous vous recommandons de ne pas utiliser les fonctions **ScrollWindow** et **ScrollWindowEx** de GDI, et à la place de redessiner le contenu GDI et Direct3D à l’écran en réponse au défilement.
-   Utilisez Flip Model dans un [**HWND**](../winprog/windows-data-types.md) qui n’est pas également ciblé par d’autres API, y compris le modèle de présentation dxgi BitBlt, d’autres versions de Direct3D ou GDI. Étant donné que le modèle BitBlt gère une copie supplémentaire de la surface, vous pouvez ajouter GDI et d’autres contenus Direct3D au même **HWND** par le biais de mises à jour ponctuelles à partir de Direct3D et GDI. Lorsque vous utilisez le modèle de retournement, seul le contenu Direct3D dans le modèle de retournement de chaînes que le runtime passe à DWM est visible. Le runtime ignore toutes les autres mises à jour du contenu Direct3D ou GDI du modèle BitBlt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Synchronisation des frames des applications DXGI Flip Model

Les statistiques présentent les informations de minutage des trames utilisées par les applications multimédias pour synchroniser les flux vidéo et audio et récupérer des problèmes de lecture vidéo. Les applications peuvent utiliser les informations de minutage de trame dans les statistiques actuelles pour ajuster la vitesse de présentation de leurs images vidéo pour une présentation plus lisse. Pour obtenir les informations statistiques de présentation, appelez la méthode [**IDXGISwapChain :: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) pour obtenir la structure des [**\_ \_ statistiques du frame dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . **Dxgi \_ Les \_ statistiques de frame** contiennent des statistiques sur [**IDXGISwapChain1 : les appels resent1 :P**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Une chaîne de permuter le modèle fournit des informations statistiques en mode fenêtre et plein écran. Pour les chaînes d’échange de modèle BitBlt en mode fenêtre, toutes les valeurs des **\_ \_ statistiques de frame dxgi** sont des zéros.

Pour les statistiques de modèle de retournement, [**IDXGISwapChain :: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) retourne les **statistiques de \_ trame d’erreur dxgi \_ \_ \_ disjointes** dans les situations suivantes :

-   Premier appel à [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics), qui indique le début d’une séquence
-   Changement de mode : mode avec fenêtre, en mode plein écran ou plein écran pour les transitions en plein écran

Les valeurs des membres **PresentRefreshCount**, **SyncRefreshCount** et **SyncQPCTime** des [**\_ \_ statistiques de frame dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) présentent les caractéristiques suivantes :

-   **PresentRefreshCount** est égal à **SyncRefreshCount** lorsque l’application présente sur chaque Vsync.
-   **SyncRefreshCount** est obtenu à l’intervalle Vsync lorsque le présent a été envoyé, **SyncQPCTime** est approximativement l’heure associée à l’intervalle de Vsync.

La méthode [**IDXGISwapChain :: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) retourne le dernier nombre présent, autrement dit, l’ID actuel du dernier IDXGISwapChain1 réussi [**::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) appel effectué par un périphérique d’affichage associé à la chaîne de permutation. Cet ID est la valeur du membre **PresentCount** de la structure de [**\_ \_ statistiques de frame dxgi**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . Pour les chaînes de swap du modèle BitBlt, en mode fenêtre, toutes les valeurs des **\_ \_ statistiques de frame dxgi** sont des zéros.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Prévention, détection et récupération à partir de problèmes

Procédez comme suit pour éviter, détecter et récupérer des problèmes dans la présentation du cadre :

1.  Queue [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) appelle (autrement dit, appelez **IDXGISwapChain1 ::P resent1** plusieurs fois, ce qui entraîne leur collecte dans une file d’attente).
2.  Créez une structure de file d’attente présente pour stocker tous les [**:P IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)de mise à l’erreur de l’resent1 de l’ID actuel (retourné par [**IDXGISwapChain :: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) et les valeurs de **PresentRefreshCount** associées, calculées/attendues.
3.  Pour détecter un problème :

    -   Appelez [**IDXGISwapChain :: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Pour ce frame, récupérez l’ID actuel (**PresentCount**) et le nombre de Vsync où le système d’exploitation a présenté la dernière image au moniteur (**PresentRefreshCount**).
    -   Récupérez le **PresentRefreshCount** attendu qui est associé à l’ID présent et que vous avez précédemment stocké dans la structure de la file d’attente actuelle.
    -   Si le **PresentRefreshCount** réel est postérieur au **PresentRefreshCount** attendu, un problème s’est produit.

4.  Pour récupérer à partir du problème :

    -   Calculez le nombre de trames à ignorer pour récupérer du problème. Par exemple, si l’étape 3 révèle que le nombre Vsync attendu (**PresentRefreshCount**) pour un ID actuel (**PresentCount**) est 5 et que le nombre réel de Vsync pour l’ID actuel est de 8, le nombre de frames à ignorer pour récupérer du problème est de 3 frames.
    -   Passez 0 au paramètre *SyncInterval* dans ce nombre d’appels à [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) pour ignorer ce nombre de frames.

        > [!Note]  
        > Si le problème est constitué d’un grand nombre de frames, appelez [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) avec le paramètre *Flags* défini à [**dxgi \_ \_ restart**](dxgi-present.md) pour ignorer et ignorer tous les cadeaux en attente.

         

Voici un exemple de scénario de récupération à partir de défauts dans une présentation de cadre :

![illustration d’un exemple de scénario de récupération à partir de défauts dans une présentation de cadre](images/frame-sync-glitch-recover.png)

Dans l’exemple de scénario, vous vous attendez à ce que frame A s’affiche à l’écran sur un nombre Vsync de 1. Toutefois, vous détectez en fait le nombre de Vsync que le frame A affiche à l’écran 4. Par conséquent, vous déterminez qu’un problème s’est produit. Vous pouvez ensuite ignorer 3 frames, autrement dit, vous pouvez passer 0 au paramètre *SyncInterval* dans 3 appels à [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Dans l’exemple de scénario précédent, pour récupérer du problème, vous avez besoin d’un total de 8 **IDXGISwapChain1 ::P appels resent1** . Le 9e frame est ensuite visible selon le nombre de Vsync que vous attendez.

Voici une chronologie des événements de présentation. Chaque ligne verticale représente un Vsync. Le sens horizontal est l’heure, qui s’étend vers la droite. Vous pouvez utiliser la figure pour imaginer comment les problèmes peuvent se produire.

![illustration d’une chronologie d’événements de présentation](images/present-timeline.png)

La figure illustre cette séquence :

1.  L’application est en éveil sur Vsync, restitue le bleu, appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), puis revient en mode veille.
2.  L’unité de traitement graphique (GPU) sort de l’inactivité, effectue le rendu en bleu, puis revient en mode veille.
3.  Le DWM se réveille à la Vsync suivante, compose le bleu dans sa mémoire tampon d’arrière-plan, appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), puis revient en mode veille.
4.  L’application est en éveil, restitue le vert, appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), puis revient en mode veille.
    > [!Note]  
    > L’application s’exécute simultanément pendant que le GPU effectue le compose du bleu.

     

5.  Ensuite, le GPU restitue le vert pour l’application.
6.  Enfin, le convertisseur numérique à analogique (DAC) affiche les résultats de la composition DWM sur le moniteur sur le Vsync suivant.

À partir de la chronologie, vous pouvez imaginer la latence des statistiques actuelles et la façon dont les problèmes peuvent se produire. Par exemple, pour afficher un problème DWM pour la couleur verte apparaissant à l’écran, Imaginez l’élargissement de la zone verte/rouge afin que le côté droit de la zone verte/rouge corresponde à l’extrémité droite de la zone violette/rouge. Dans ce scénario, la DAC affiche deux frames bleus, puis le cadre vert. Vous pouvez voir que ce problème s’est produit lors de la lecture des statistiques actuelles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration de la présentation avec le modèle de retournement, les rectangles modifiés et les zones défilantes](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
