---
description: Pour améliorer les performances, vous souhaiterez peut-être créer plusieurs chaînes de permutation par périphérique de rendu Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Amélioration des performances avec plusieurs chaînes de permutation par appareil de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91445660bf9efc59e9e39c88819587dce3960325df0659487eaae67a845a7329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627489"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Amélioration des performances avec plusieurs chaînes de permutation par appareil de rendu

Pour améliorer les performances, vous souhaiterez peut-être créer plusieurs chaînes de permutation par périphérique de rendu Direct3D. Utilisez cette approche pour économiser la mémoire requise en créant des appareils supplémentaires, ou pour réduire la quantité de temps de rendu à afficher séparément dans les chaînes de permutation individuelles, ou pour économiser la mémoire et réduire le temps de rendu.

-   [Scénarios d’application avec plusieurs chaînes de permutation par appareil](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Gestion de plusieurs chaînes de permutation par appareil](#managing-multiple-swap-chains-per-device)
    -   [Définition de la latence de trame maximale](#setting-maximum-frame-latency)
    -   [Utilisation de Flip Model avec plusieurs chaînes de permutation par appareil](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Rubriques connexes](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Scénarios d’application avec plusieurs chaînes de permutation par appareil

Envisagez d’utiliser plusieurs chaînes lorsque la scène de l’application se compose d’objets d’affichage distincts qui sont rendus et mis à jour indépendamment. Par exemple, l’application change constamment d’animation, telle qu’une vidéo d’un côté et un texte défilant sur un autre côté. Pour économiser de la mémoire qui devrait normalement créer un appareil supplémentaire et faciliter le partage de contenu entre les deux chaînes de permutation, vous pouvez créer des chaînes de permutation liées au même appareil de rendu Direct3D. Utilisez une chaîne de permutation pour l’animation et une chaîne de permutation pour le texte. Un exemple courant de ce scénario est une application Direct3D qui utilise également l’API [DirectComposition](../directcomp/directcomposition-portal.md) .

Un autre scénario est lorsque vous souhaitez économiser le temps de rendu en définissant plusieurs cibles de rendu sur plusieurs chaînes de permutation simultanément. Supposons, par exemple, que vous souhaitiez afficher une scène complexe avec un grand nombre de textures et de géométries, telles que des voitures de course sur une piste, et que vous souhaitiez que la fenêtre d’application affiche les vues des deux miroirs d’arrière-plan et latéraux dans deux fenêtres d’affichage qui sont restituées par deux chaînes d’échange. Si vous définissez plusieurs chaînes de permutation comme cibles de rendu, votre application n’a pas besoin de répéter les temps de rendu sur chaque chaîne de permutation séparément.

## <a name="managing-multiple-swap-chains-per-device"></a>Gestion de plusieurs chaînes de permutation par appareil

Utilisez les instructions de cette section pour gérer plusieurs chaînes de permutation que vous créez pour un seul appareil de rendu Direct3D.

### <a name="setting-maximum-frame-latency"></a>Définition de la latence de trame maximale

Utilisez la méthode [**IDXGIDevice1 :: SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) pour définir le nombre maximal d’opérations présentes que le système d’exploitation peut mettre en file d’attente pour le rendu de l’affichage. Ce nombre maximal est par périphérique de rendu Direct3D plutôt que par chaîne de permutation. Par conséquent, pour s’assurer que le système d’exploitation affiche les opérations présentes à l’intervalle Vsync prévu, nous vous recommandons de ne pas définir la latence de trame maximale sur 1 lorsque vous créez plusieurs chaînes d’échange de modèles Flip ou BitBlt par appareil et lorsque plusieurs de ces chaînes d’échange sont rendues pour chaque trame. En règle générale, si vous soumettez de manière fiable uniquement 2 opérations présentes par trame entre toutes les chaînes de permutation du même appareil, vous pouvez définir la latence de trame maximale sur 2. Si vous ne pouvez pas envoyer et compter en toute fiabilité les opérations présentes par trame, vous pouvez utiliser les [statistiques actuelles](dxgi-flip-model.md) pour suivre le moment où le système d’exploitation affiche les opérations présentes.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Utilisation de Flip Model avec plusieurs chaînes de permutation par appareil

Utilisez ces instructions lorsque vous utilisez le [modèle de retournement dxgi](dxgi-flip-model.md) avec plusieurs chaînes de permutation que vous créez pour un seul appareil de rendu Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Ciblage d’intervalles de Vsync spécifiques avec les opérations présentes de la chaîne de permutation

Lorsque vous créez au moins deux chaînes de permutation de modèle par appareil, faites attention aux différences d’affichage lorsque vous gérez la séquence de l’état de l’appareil et la séquence d’appels à la méthode [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) de toutes les chaînes de permutation. Pour vous assurer que le système d’exploitation affiche chaque opération présente de chaîne de permutation à l’intervalle de Vsync prévu, nous vous recommandons de vous assurer que le nombre d’opérations présentes en file d’attente est toujours au moins inférieur au nombre de mémoires tampons d’arrière-plan pour la chaîne de permutation avec le moins de mémoires tampons d’arrière-plan.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Retourner les chaînes d’échange de modèle avec deux mémoires tampons

Votre application peut cibler des intervalles Vsync spécifiques quand son nombre d’opérations présentes en file d’attente est inférieur ou égal au nombre de mémoires tampons d’arrière-plan – 1. En outre, vous devez utiliser ou rendre chaque chaîne de permutation séparément, puis mettre fin à l’utilisation de chaque chaîne de permutation avec une opération présente. Ainsi, lorsque vous soumettez chaque opération actuelle pour une chaîne de permutation de modèle à 2 tampons, vous atteignez le seuil du nombre de mémoires tampons d’arrière-plan pour lesquelles vous devez être particulièrement attentif si vous souhaitez que votre application cible des intervalles Vsync spécifiques.

Dans le cas de chaînes d’échange de 2 tampons, pour cibler des intervalles de Vsync spécifiques, vous devez vous assurer que le système d’exploitation termine l’affichage de chaque opération présente de chaîne d’échange avant le rendu dans la mémoire tampon suivante. Nous vous recommandons de terminer la définition de l’affichage de la cible de rendu et de l’autre État de rendu, le rendu suivant, puis d’appeler [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) pour chacune des deux mémoires tampons d’une chaîne de permutation avant de faire de même pour une autre chaîne de permutation. Lorsque vous utilisez au moins deux chaînes de permutation, vous devez réinitialiser la cible de rendu et l’état de rendu sur l’appareil pour chaque chaîne de permutation. L’avantage de cette approche est d’éviter le cas où une ou plusieurs des opérations présentes de la chaîne de permutation manquent l’intervalle de Vsync prévu. Pour le premier exemple, application avec modification de l’animation et du texte, comme décrit dans [scénarios d’application avec plusieurs chaînes de permutation par appareil](#app-scenarios-with-multiple-swap-chains-per-device), en ciblant des intervalles présents spécifiques, vous êtes assuré que lorsque l’animation est mise à jour dans une fenêtre d’affichage, le texte correspondant restitué par une chaîne de permutation distincte est également affiché en même temps dans une autre fenêtre d’affichage. Si votre application doit cibler des intervalles Vsync spécifiques, vous devez suivre ces instructions.

Ce diagramme illustre un exemple du déroulement du code du rendu de chaîne d’échange et de la présentation dans une application avec deux chaînes de permutation de modèle avec deux mémoires tampons. Dans ce cas, vous devez cibler un intervalle présent spécifique pour chaque opération présente.

![illustration d’un modèle de basculement avec deux mémoires tampons](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Réduction du temps de rendu en définissant simultanément plusieurs chaînes de permutation en tant que cibles de rendu

Pour le deuxième exemple, course Cars sur une piste, comme décrit dans [scénarios d’application avec plusieurs chaînes de permutation par appareil](#app-scenarios-with-multiple-swap-chains-per-device), vous souhaiterez peut-être compenser le ciblage de plusieurs intervalles de Vsync à l’aide des économies de temps de rendu que vous obtenez en définissant plusieurs cibles de rendu simultanément sur toutes les chaînes de permutation. Dans ce cas, définissez plusieurs cibles de rendu simultanément, affichez la scène sur chaque chaîne de permutation, puis appelez [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) sur chaque chaîne de permutation utilisée dans la scène. L’avantage de cette approche est que vous réduisez le temps de rendu. La limitation de cette approche est que vos opérations de chaîne d’échange simultanée ne peuvent pas cibler le même Vsync quand vous utilisez des chaînes d’échange à 2 tampons. Par exemple, le système d’exploitation n’affiche pas le contenu des miroirs de la voiture de course jusqu’à 1 Vsync après que le même contenu a été vu du miroir de la vue en voiture de course.

Ce diagramme illustre un exemple du déroulement du code du rendu de chaîne d’échange et de la présentation dans une application avec deux chaînes de permutation de modèle avec deux mémoires tampons. Dans ce type d’exemple, vous enregistrez les durées de rendu dans les chaînes de permutation 1 et 2 pour les tampons A et C. Toutefois, vous ne pouvez pas synchroniser les intervalles Vsync auxquels les opérations présentes pour les mémoires tampons A et C sont affichées. Ce modèle se répète pour le frame 2.

![illustration de la définition simultanée de plusieurs chaînes de permutation en tant que cibles de rendu](images/multi-swap-chains-as-render-targets.png)

Pour éviter l’absence de l’intervalle Vsync prévu en raison de à de nombreuses opérations présentes en file d’attente, vous pouvez augmenter le nombre de mémoires tampons d’arrière-plan dans chaque chaîne de permutation. Toutefois, cette technique utilise davantage de mémoire vidéo. Pour éviter les intervalles Vsync cibles manquants, nous vous recommandons de toujours conserver le nombre d’opérations de mise en file d’attente présentes inférieures au nombre de mémoires tampons d’arrière-plan dans la chaîne de permutation avec le moins de mémoires tampons d’arrière-plan. Lorsque vous définissez deux chaînes de permutation en tant que cibles de rendu multiples, parce que vous devez mettre en file d’attente deux opérations présentes simultanément sur les deux chaînes de permutation, nous vous recommandons de créer des chaînes de permutation avec au moins trois tampons de longueur.

Le diagramme suivant montre un exemple du déroulement du code du rendu de chaîne d’échange et de la présentation dans une application avec deux chaînes de permutation de modèle avec trois mémoires tampons. Ici, étant donné que le nombre de cadeaux en file d’attente pour une trame particulière est 2, ce qui est inférieur au nombre de mémoires tampons d’arrière-plan par chaîne de permutation, votre application peut définir plusieurs cibles de rendu et cibler toujours les mêmes intervalles Vsync pour les tampons A et D dans le frame 2 et pour les mémoires tampons dans les frames suivants.

![illustration de la définition simultanée de plusieurs chaînes de permutation comme cibles de rendu ciblant le même vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration de la présentation avec le modèle de retournement, les rectangles modifiés et les zones défilantes](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
