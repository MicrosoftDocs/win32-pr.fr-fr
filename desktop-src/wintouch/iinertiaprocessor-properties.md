---
title: Propriétés (IInertiaProcessor)
description: Cette section contient les propriétés de l’interface IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Interface tactile, IInertiaProcessor
- Windows Tactile, propriétés d’interface
- inertie, interface IInertiaProcessor
- IInertiaProcessor, interface, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7825a97545c897f402144ce5113b79650b9eba31e19da7ceef1459ae6cdc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030123"
---
# <a name="properties-iinertiaprocessor"></a>Propriétés (IInertiaProcessor)

Cette section contient les propriétés de l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Propriété                                                                               | Description                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Spécifie l’emplacement horizontal de départ pour une cible avec intertia.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Spécifie l’emplacement vertical de début d’une cible avec intertia.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Spécifie le mouvement initial de l’objet cible sur l’axe horizontal.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Spécifie le mouvement initial de l’objet cible sur l’axe vertical.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Spécifie la vélocité de rotation de la cible au début du mouvement.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Spécifie le taux d’expansion RADIUS de la cible au début du déplacement.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Spécifie la distance entre le bord de la cible et son centre avant la modification de l’objet.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Limite la distance vers la gauche de l’écran que l’objet cible peut déplacer.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Limite la distance vers le haut de l’écran que l’objet cible peut déplacer.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Limite le déplacement de l’objet cible vers le côté droit de l’écran.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Limite la distance vers le bas de l’écran que l’objet cible peut déplacer.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Spécifie la région la plus à gauche pour rebondir l’objet cible.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Spécifie la région de premier plan pour le rebond de l’objet cible.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Spécifie la région la plus à droite pour rebondir l’objet cible.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Spécifie la région inférieure pour le rebond de l’objet cible.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Spécifie le taux souhaité que l’objet cible arrêtera de tourner en radians par ms.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Spécifie la distance souhaitée (en radians) qu’un objet sera manipulé par le processeur d’inertie. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Spécifie la modification souhaitée dans le rayon moyen de l’objet.                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Spécifie la fréquence d’arrêt du développement de l’objet.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Spécifie la fréquence souhaitée à laquelle les opérations de traduction sont ralenties.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Spécifie la distance souhaitée de l’objet.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Spécifie l’horodatage de début d’un objet cible qui a une inertie.                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




