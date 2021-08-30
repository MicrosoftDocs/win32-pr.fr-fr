---
description: Événements de source de média
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Événements de source de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee97d0d13aa96b4b0c480535836e827e9cdea47a551c371082d71a65c1c8021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941639"
---
# <a name="media-source-events"></a>Événements de source de média

Cette rubrique répertorie les événements qui sont envoyés par les sources de média et les flux multimédias. Les sources multimédias peuvent également envoyer des événements personnalisés qui ne sont pas répertoriés ici.

## <a name="media-source-events"></a>Événements de source de média



| Événement                                                                      | Description                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Événement MEEndOfPresentation](meendofpresentation.md)                       | La présentation s’est terminée. Tous les flux de la présentation ont atteint la fin du flux.      |
| [Événement MENewStream](menewstream.md)                                       | Un nouveau flux a été créé. L’événement contient un pointeur vers le flux.                            |
| [Événement MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) | Les caractéristiques de la source ont changé. (Facultatif.)                                      |
| [Événement MESourceMetadataChanged](mesourcemetadatachanged.md)               | Les métadonnées de la source ont été modifiées. (Facultatif.)                                                   |
| [Événement MESourcePaused](mesourcepaused.md)                                 | La source a été suspendue. Toutes les sources ne prennent pas en charge la suspension.                                          |
| [Événement MESourceRateChanged](mesourceratechanged.md)                       | La vitesse de lecture de la source a changé. (Facultatif ; s’applique si la source prend en charge le contrôle de fréquence.) |
| [Événement MESourceRateChangeRequested](mesourceratechangerequested.md)       | La source demande un nouveau taux de lecture. (Facultatif.)                                        |
| [Événement MESourceSeeked](mesourceseeked.md)                                 | La source a été recherchée. Toutes les sources ne prennent pas en charge la recherche.                                          |
| [Événement MESourceStarted](mesourcestarted.md)                               | La source a été démarrée.                                                                          |
| [Événement MESourceStopped](mesourcestopped.md)                               | La source a été arrêtée.                                                                          |
| [Événement MEUpdatedStream](meupdatedstream.md)                               | Un flux existant a été cherché ou redémarré. L’événement contient un pointeur vers le flux.         |



 

## <a name="media-stream-events"></a>Événements de flux multimédia



| Événement                                                    | Description                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Événement MEEndOfStream](meendofstream.md)                 | Le flux s’est terminé.                                                                                                              |
| [Événement MEError](meerror.md)                             | Une erreur s’est produite lors de la diffusion en continu. Utilisez cet événement pour les erreurs qui ne sont pas liées à l’un des autres événements répertoriés ici. |
| [Événement MEMediaSample](memediasample.md)                 | Le flux a généré un nouvel exemple.                                                                                         |
| [Événement MEStreamFormatChanged](mestreamformatchanged.md) | Le type de média a changé. (Facultatif.)                                                                                        |
| [Événement MEStreamPaused](mestreampaused.md)               | Le flux a été suspendu.                                                                                                         |
| [Événement MEStreamSeeked](mestreamseeked.md)               | Le flux a été cherché.                                                                                                         |
| [Événement MEStreamStarted](mestreamstarted.md)             | Le flux a été démarré.                                                                                                        |
| [Événement MEStreamStopped](mestreamstopped.md)             | Le flux a été arrêté.                                                                                                        |
| [Événement MEStreamThinMode](mestreamthinmode.md)           | Le mode de réduction a démarré ou s’est arrêté. (Facultatif.)                                                                              |
| [Événement MEStreamTick](mestreamtick.md)                   | Il y a un intervalle dans le flux. (Facultatif.)                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> </dl>

 

 



