---
title: Constantes (informations de référence sur les animations Windows)
description: Documentation de référence pour les constantes et énumérations définies par le gestionnaire d’animations Windows.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2cceae981ea7cc0e2b78d9dadbea88075eb3ad
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106539003"
---
# <a name="constants-windows-animation-reference"></a>Constantes (informations de référence sur les animations Windows)

Documentation de référence pour les constantes et énumérations définies par le gestionnaire d’animations Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                             | Description                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DIMENSION d’animation d’IU \_ \_ \_ inconnue**](ui-animation-dimension-unknown.md)<br/>                                            | Indique que la dimension demandée ne peut pas être récupérée.<br/>                                                                                                                                                                                                     |
| [**itération de l’animation d’IU \_ \_ \_ aucune**](-ui-animation-iteration-none.md)<br/>                                                 | Indique qu’il s’agit de l’entrée initiale dans une boucle donnée.<br/>                                                                                                                                                                                                     |
| [**\_démarrage du \_ Storyboard d’image clé de \_ l’interface utilisateur \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Représente l’image clé implicite au début de chaque Storyboard.<br/>                                                                                                                                                                                              |
| [**l’animation de l’interface utilisateur se \_ \_ répète \_ indéfiniment**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) soit appelée.<br/>                                                            |
| [**l’animation de l’interface utilisateur se \_ \_ \_ TERMINe indéfiniment \_ à la \_ \_ fin**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la boucle KeyFrame se termine sur l’image clé de fin lorsque la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) est appelée.<br/>   |
| [**L’animation d’IU se \_ \_ répète \_ indéfiniment \_ \_ au \_ début**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la boucle KeyFrame se termine sur l’image clé de départ lorsque la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) est appelée.<br/> |
| [**\_secondes d’animation de l’interface utilisateur \_ \_**](ui-animation-seconds-eventually.md)<br/>                                          | Indique que l’animation Windows peut retarder le démarrage planifié d’un Storyboard pour autant de temps que nécessaire pour éviter les conflits de planification.<br/>                                                                                                                     |
| [**ANIMATION de l’interface utilisateur- \_ \_ secondes \_ infinies**](ui-animation-seconds-infinite.md)<br/>                                              | Indique qu’il n’y a aucun événement planifié.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les animations Windows](windows-animation-reference.md)
</dt> </dl>

 

