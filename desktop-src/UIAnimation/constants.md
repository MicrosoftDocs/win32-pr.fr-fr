---
title: constantes (Windows référence d’Animation)
description: documentation de référence pour les constantes et les énumérations définies par le gestionnaire d’animations Windows.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23964a2936b3879d551bcde9c2c25c2d63465e1cb4afb07cee25a3ce74a2a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419121"
---
# <a name="constants-windows-animation-reference"></a>constantes (Windows référence d’Animation)

documentation de référence pour les constantes et les énumérations définies par le gestionnaire d’animations Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                             | Description                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DIMENSION d’animation d’IU \_ \_ \_ inconnue**](ui-animation-dimension-unknown.md)<br/>                                            | Indique que la dimension demandée ne peut pas être récupérée.<br/>                                                                                                                                                                                                     |
| [**itération de l’animation d’IU \_ \_ \_ aucune**](-ui-animation-iteration-none.md)<br/>                                                 | Indique qu’il s’agit de l’entrée initiale dans une boucle donnée.<br/>                                                                                                                                                                                                     |
| [**\_démarrage du \_ Storyboard d’image clé de \_ l’interface utilisateur \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Représente l’image clé implicite au début de chaque Storyboard.<br/>                                                                                                                                                                                              |
| [**l’animation de l’interface utilisateur se \_ \_ répète \_ indéfiniment**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) soit appelée.<br/>                                                            |
| [**l’animation de l’interface utilisateur se \_ \_ \_ TERMINe indéfiniment \_ à la \_ \_ fin**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la boucle KeyFrame se termine sur l’image clé de fin lorsque la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) est appelée.<br/>   |
| [**L’animation d’IU se \_ \_ répète \_ indéfiniment \_ \_ au \_ début**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indique que l’intervalle entre deux images clés dans un Storyboard doit se répéter indéfiniment jusqu’à ce que la boucle KeyFrame se termine sur l’image clé de départ lorsque la méthode [**IUIAnimationStoryboard :: conclut**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) est appelée.<br/> |
| [**\_secondes d’animation de l’interface utilisateur \_ \_**](ui-animation-seconds-eventually.md)<br/>                                          | indique que Windows Animation peut retarder le démarrage planifié d’un storyboard pour autant de temps que nécessaire pour éviter les conflits de planification.<br/>                                                                                                                     |
| [**ANIMATION de l’interface utilisateur- \_ \_ secondes \_ infinies**](ui-animation-seconds-infinite.md)<br/>                                              | Indique qu’il n’y a aucun événement planifié.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Référence d’animation](windows-animation-reference.md)
</dt> </dl>

 

