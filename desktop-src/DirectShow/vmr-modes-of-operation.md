---
description: Modes de fonctionnement VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modes de fonctionnement VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524520"
---
# <a name="vmr-modes-of-operation"></a>Modes de fonctionnement VMR

L’architecture du composant VMR permet aux applications de les configurer de différentes manières, en fonction de la façon dont le rendu doit être effectué. Le tableau suivant présente les trois modes de présentation et les deux modes de mixage, ainsi que les composants qui sont présents pour chaque configuration.



| Mode       | Flux unique                                                                     | Plusieurs flux (mode de mixage)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Fenêtrées   | Allocator-unité de synchronisation presenterCore<br/> Gestionnaire de fenêtres<br/> | MixerCompositor\*<br/> Allocator-présentateur<br/> Unité de synchronisation principale<br/> Gestionnaire de fenêtres<br/> |
| Sans fenêtre | Allocator-unité de synchronisation presenterCore<br/>                           | MixerCompositor\*<br/> Allocator-présentateur<br/> Unité de synchronisation principale<br/>                           |
| Rendu | Allocator-Presenter (fourni par l’application) unité de synchronisation principale<br/> | MixerCompositor\*<br/> Allocator-Presenter (fourni par l’application)<br/> Unité de synchronisation principale<br/> |



 

\* Indique que l’application a la possibilité de fournir un composant personnalisé ou d’utiliser le composant par défaut.

Dans toutes les configurations, le point principal à retenir lorsque vous créez des graphiques de filtre avec VMR est que vous devez configurer VMR avant de le connecter.

Pour toutes les configurations, les codes confidentiels ne peuvent pas être ajoutés ou supprimés de manière dynamique une fois que VMR est connecté au filtre en amont, mais ils peuvent être connectés et déconnectés. Si l’application ne peut pas savoir combien de codes confidentiels seront nécessaires, elle doit configurer VMR pour le nombre maximal qui peut être nécessaire. La présence de broches d’entrée inutilisées sur le filtre ne dégrade pas les performances de rendu. Contrairement à l’ancien mélangeur de superposition, VMR n’a pas de broche de sortie, car il ne nécessite pas de filtre distinct pour la gestion des fenêtres.

Les sections suivantes décrivent comment configurer VMR pour un mode donné :

-   [Mode avec fenêtres VMR (compatibilité)](vmr-windowed--compatibility--mode.md)
-   [Mode sans fenêtre VMR](vmr-windowless-mode.md)
-   [VMR avec plusieurs flux (mode de mixage)](vmr-with-multiple-streams--mixing-mode.md)
-   [Mode de mixage YUV](yuv-mixing-mode.md)
-   [Positionnement et déplacement de rectangles vidéo dans l’espace de composition](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Mode exclusif DirectDraw](directdraw-exclusive-mode.md)

 

 




