---
description: Codes de notification des événements DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Codes de notification des événements DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717c260c84a1038860ee04f46db6224025b7709c3ad039e7625a48ae6359cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686449"
---
# <a name="dvd-event-notification-codes"></a>Codes de notification des événements DVD

Cette section répertorie les codes de notification d’événement pour la lecture et la navigation sur DVD dans DirectShow.

pour plus d’informations sur la réception d’événements dans DirectShow, consultez [Notification d’événements dans DirectShow](event-notification-in-directshow.md).

Pour les autres codes d’événement non-DVD, consultez [codes de notification d’événement](event-notification-codes.md).



| Code de notification d’événement                                                        | Description                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_changement d' \_ angle de DVD EC \_**](ec-dvd-angle-change.md)                          | Signale que le nombre d’angles disponibles a changé ou que le numéro d’angle actuel a changé.                                                                      |
| [**\_angles de DVD EC \_ \_ disponibles**](ec-dvd-angles-available.md)                  | Indique si un bloc angle est lu et si des modifications d’angle peuvent être effectuées.                                                                                      |
| [**\_modification du \_ \_ flux audio du DVD \_ EC**](ec-dvd-audio-stream-change.md)           | Signale que le numéro de flux audio actuel a changé pour le titre principal.                                                                                                  |
| [**\_BeginNavigationCommands de DVD EC \_**](ec-dvd-beginnavigationcommands.md)     | Envoyé lors du démarrage d’un jeu de commandes de navigation sur DVD.                                                                                                                  |
| [**\_bouton DVD \_ EC \_ \_ activé automatiquement**](ec-dvd-button-auto-activated.md)       | Signale qu’un bouton de menu a été automatiquement activé par des instructions sur le disque.                                                                                 |
| [**\_changement du \_ bouton \_ DVD EC**](ec-dvd-button-change.md)                        | Signale que le nombre de boutons disponibles a changé ou que le numéro de bouton actuellement sélectionné a changé.                                                         |
| [**\_arrêt du \_ chapitre du DVD ce \_**](ec-dvd-chapter-autostop.md)                  | Indique que la lecture s’est arrêtée à la suite d’un appel à la méthode [**IDvdControl2 ::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .                    |
| [**\_début du \_ chapitre du DVD EC \_**](ec-dvd-chapter-start.md)                        | Signale que le navigateur DVD a commencé la lecture d’un nouveau chapitre dans le titre actuel.                                                                                    |
| [**démarrage de la \_ commande de DVD EC \_ \_**](ec-dvd-cmd-start.md)                                | Signale qu’une commande particulière a commencé.                                                                                                                              |
| [**fin de la commande de DVD de la EC \_ \_ \_**](ec-dvd-cmd-end.md)                                    | Signale qu’une commande particulière est terminée.                                                                                                                          |
| [**\_ \_ \_ temps HMSF actuel du \_ DVD**](ec-dvd-current-hmsf-time.md)               | Signale l’heure actuelle dans le format de [**\_ \_ code temporel DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) au début de chaque unité d’objet vidéo (VOBU).                                   |
| [**\_ \_ heure actuelle du DVD EC \_**](ec-dvd-current-time.md)                          | Signale le début de chaque VOBU.                                                                                                                                      |
| [**\_disque DVD d’EC \_ \_ éjecté**](ec-dvd-disc-ejected.md)                          | Signale qu’un disque a été éjecté du lecteur.                                                                                                                      |
| [**\_disque DVD-EC \_ \_ inséré**](ec-dvd-disc-inserted.md)                        | Signale qu’un disque a été inséré dans le lecteur.                                                                                                                     |
| [**\_modification du \_ domaine du DVD EC \_**](ec-dvd-domain-change.md)                        | Indique le nouveau domaine du navigateur DVD.                                                                                                                                 |
| [**\_erreur de DVD EC \_**](ec-dvd-error.md)                                         | Signale une condition d’erreur de DVD.                                                                                                                                            |
| [**\_Modification de \_ GPRM de DVD EC \_**](ec-dvd-gprm-change.md)                            | Envoyé lorsque la valeur d’un registre de paramètres général (GPRM) change.                                                                                                       |
| [**\_ \_ mode karaoké du DVD EC \_**](ec-dvd-karaoke-mode.md)                          | Indique que le navigateur a commencé à exécuter ou à terminer de relire les données du karaoké.                                                                                   |
| [**\_NavigationCommand de DVD EC \_**](ec-dvd-navigationcommand.md)                 | Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) traite une commande de navigation sur DVD.                                                                               |
| [**\_DVD EC \_ non \_ FP PF \_**](ec-dvd-no-fp-pgc.md)                               | Indique que le disque DVD ne dispose pas d’un FP \_ PGC (première chaîne de programme de lecture).                                                                                           |
| [**\_modification du \_ \_ niveau parental du DVD \_ EC**](ec-dvd-parental-level-change.md)       | Signale que le niveau parental du contenu créé va être modifié.                                                                                               |
| [**\_changement du \_ taux de lecture des DVD EC \_ \_**](ec-dvd-playback-rate-change.md)         | Indique qu’une modification de la vitesse de lecture a été lancée et que le nouveau taux est dans le paramètre.                                                                            |
| [**\_lecture du DVD EC \_ \_ arrêtée**](ec-dvd-playback-stopped.md)                  | Indique que la lecture a été arrêtée. Le navigateur DVD a terminé la lecture du titre et n’a trouvé aucune autre instruction de branchement pour la lecture suivante. |
| [**\_arrêt du \_ PLAYPERIOD de DVD EC \_**](ec-dvd-playperiod-autostop.md)            | Indique que le navigateur a fini de reproduire le segment spécifié dans un appel à PlayPeriodInTitleAutoStop.                                                           |
| [**\_modification des \_ cellules du programme de DVD EC \_ \_**](ec-dvd-program-cell-change.md)           | Envoyé lorsque le numéro de programme DVD ou le numéro de cellule change.                                                                                                                  |
| [**\_changement de \_ chaîne du programme de DVD EC \_ \_**](ec-dvd-program-chain-change.md)         | Envoyé lorsque la chaîne de programme active (PGC) est modifiée.                                                                                                                            |
| [**\_Modification de \_ SPRM de DVD EC \_**](ec-dvd-sprm-change.md)                            | Envoyé lorsque la valeur d’un registre de paramètres système (SPRM) change.                                                                                                        |
| [**\_DVD ce \_ toujours \_ désactivé**](ec-dvd-still-off.md)                                | Signale la fin de tout encore.                                                                                                                                             |
| [**\_DVD EC \_ toujours \_ allumé**](ec-dvd-still-on.md)                                  | Signale le début de tout encore.                                                                                                                                       |
| [**modification du flux de sous- \_ image de DVD EC \_ \_ \_**](ec-dvd-subpicture-stream-change.md) | Signale que le numéro de flux de sous-image actuel a changé pour le titre principal.                                                                                             |
| [**\_modification du \_ jeu de titres du DVD EC \_ \_**](ec-dvd-title-set-change.md)                 | Envoyé lorsque le titre de la vidéo active (STM) change.                                                                                                                          |
| [**\_modification du \_ titre du DVD EC \_**](ec-dvd-title-change.md)                          | Indique quand le numéro de titre actuel change.                                                                                                                          |
| [**\_ \_ \_ modification UOPs valide du DVD EC \_**](ec-dvd-valid-uops-change.md)               | Signale que l’ensemble de méthodes d’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) disponibles a changé.                                                                     |
| [**\_ \_ Décalage VOBU du DVD EC \_**](ec-dvd-vobu-offset.md)                            | Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) analyse un paquet PCI.                                                                                              |
| [**\_ \_ Horodatage VOBU de DVD EC \_**](ec-dvd-vobu-timestamp.md)                      | Envoyé lorsque le [navigateur DVD](dvd-navigator-filter.md) analyse un paquet PCI.                                                                                              |
| [**\_avertissement de DVD EC \_**](ec-dvd-warning.md)                                     | Signale une condition d’avertissement de DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> </dl>

 

 



