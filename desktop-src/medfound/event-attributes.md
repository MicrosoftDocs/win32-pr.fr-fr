---
description: Attributs d'événement
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Attributs d’événement (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227772"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Attributs d’événement (Microsoft Media Foundation)

Les attributs suivants s’appliquent aux événements.



| Attribut                                                                                                        | Description                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_événement MF \_ - \_ éclaircir**](mf-event-do-thinning-attribute.md)                                                | Quand une source de média demande un nouveau taux de lecture, spécifie si la source demande également une éclaircie.                |
| [**\_ \_ nœud sortie de l’événement MF \_**](mf-event-output-node-attribute.md)                                                | Identifie le nœud de topologie d’un récepteur de flux.                                                                       |
| [**décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_**](mf-event-presentation-time-offset-attribute.md)                     | Décalage entre l’heure de présentation et les horodatages de la source du média.                                              |
| [**\_ \_ heure SCRUBSAMPLE de l’événement MF \_**](mf-event-scrubsample-time-attribute.md)                                      | Durée de présentation d’un échantillon rendu lors du nettoyage.                                                     |
| [**\_SESSIONCAPS d’événements MF \_**](mf-event-sessioncaps-attribute.md)                                                 | Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.                  |
| [**\_ \_ SESSIONCAPS Delta d’événement MF \_**](mf-event-sessioncaps-delta-attribute.md)                                    | Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle. |
| [**\_ \_ \_ début réel de la source de l’événement MF \_**](mf-event-source-actual-start-attribute.md)                               | Contient l’heure de début de redémarrage d’une source de média à partir de sa position actuelle.                                       |
| [**caractéristiques de la \_ source d’événements MF \_ \_**](mf-event-source-characteristics-attribute.md)                          | Spécifie les caractéristiques actuelles de la source du média.                                                            |
| [**caractéristiques de la \_ source d’événements MF \_ \_ \_ Old**](mf-event-source-characteristics-old-attribute.md)                 | Spécifie les caractéristiques précédentes de la source du média.                                                           |
| [**début du substitut de la \_ source d’événement MF \_ \_ \_**](mf-event-source-fake-start-attribute.md)                                   | Spécifie si la topologie du segment actuel est vide.                                                              |
| [**\_ \_ PROJECTSTART source de l’événement MF \_**](mf-event-source-projectstart-attribute.md)                                | Spécifie l’heure de début d’une topologie de segment.                                                                      |
| [**TOPOLOGIE de la \_ source d’événements MF \_ \_ \_ annulée**](mf-event-source-topology-canceled-attribute.md)                     | Spécifie si la source de Sequencer a annulé une topologie.                                                           |
| [**heure de la présentation du démarrage de l' \_ événement MF \_ \_ \_**](mf-event-start-presentation-time-attribute.md)                       | Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.               |
| [**\_ \_ \_ heure de début de la présentation de l’événement MF \_ \_ à la \_ sortie**](mf-event-start-presentation-time-at-output-attribute.md) | Heure de présentation à laquelle les récepteurs multimédia affichent le premier exemple de la nouvelle topologie.                      |
| [**État de la \_ topologie des événements MF \_ \_**](mf-event-topology-status-attribute.md)                                        | Spécifie l’état d’une topologie pendant la lecture.                                                                   |
| [**heure d’occurrence de l' \_ \_ événement d’environ session \_ \_ MF \_**](mf-session-approx-event-occurrence-time-attribute.md)        | Heure approximative à laquelle la session multimédia a déclenché un événement.                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



