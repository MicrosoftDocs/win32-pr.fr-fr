---
description: Codes de notification d’événement
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Codes de notification d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c41abc3ffc7a93a39e7a97fb210b491ad4fc58
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544569"
---
# <a name="event-notification-codes"></a>Codes de notification d’événement

Cette section répertorie les événements DirectShow qui ne sont pas spécifiques au DVD. Pour les événements spécifiques au DVD, consultez [codes de notification d’événement DVD](dvd-notification-codes.md).

Filtre les événements d’envoi au gestionnaire du graphique de filtre en appelant la méthode [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) . Le gestionnaire de graphes de filtre gère certains événements et les autres files d’attente pour l’application. L’application les récupère en appelant la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) .

Dans les sections qui suivent, chaque entrée répertorie le code d’événement, la signification des paramètres d’événement et l’action par défaut du gestionnaire de graphique de filtre pour l’événement, le cas échéant. Pour remplacer l’action par défaut, appelez [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). Les codes d’événement sont définis dans les fichiers d’en-tête Evcode. h et Audevcod. h. S’il n’y a pas d’action par défaut, le gestionnaire de graphique de filtre transfère automatiquement l’événement à l’application (via la file d’attente d’événements).

**Événements personnalisés**

Les filtres peuvent définir des événements personnalisés avec des codes d’événement dans la plage de l' \_ utilisateur EC et versions ultérieures. Le gestionnaire de graphes de filtre les place directement dans la file d’attente des événements. Toutefois, les avertissements suivants s’appliquent :

-   Le gestionnaire de graphique de filtre ne peut pas libérer les paramètres d’événement à l’aide de la méthode normal [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) . L’application doit libérer le nombre de mémoire ou de références associé aux paramètres de l’événement.
-   Le filtre doit uniquement envoyer l’événement à partir d’une application préparée pour gérer l’événement. (Peut-être que l’application peut définir une propriété personnalisée sur le filtre pour indiquer qu’il est possible d’envoyer l’événement.)



| Code de notification d’événement                                                 | Description                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**\_activation EC**](ec-activate.md)                                     | Une fenêtre vidéo est en cours d’activation ou de désactivation.                                                                         |
| [**\_BANDWIDTHCHANGE EC**](ec-bandwidthchange.md)                       | Non pris en charge.                                                                                                            |
| [**\_données de mise en mémoire tampon EC \_**](ec-buffering-data.md)                        | Le graphique met en mémoire tampon des données ou a arrêté la mise en mémoire tampon des données.                                                               |
| [**EC \_ généré**](ec-built.md)                                           | Envoyer par le contrôle Video lorsqu’un graphique a été créé. Non transmis aux applications.                                     |
| [**\_horloge EC \_ modifiée**](ec-clock-changed.md)                          | L’horloge de référence a changé.                                                                                          |
| [**horloge EC non \_ \_ définie**](ec-clock-unset.md)                              | Le fournisseur d’horloge a été déconnecté.                                                                                      |
| [**\_événement EC CODECAPI \_**](ec-codecapi-event.md)                        | Envoyé par un encodeur pour signaler un événement d’encodage.                                                                           |
| [**EC \_ complet**](ec-complete.md)                                     | Toutes les données d’un flux de données particulier ont été rendues.                                                                      |
| [**\_CONTENTPROPERTY EC \_ modifiés**](ec-contentproperty-changed.md)      | Non pris en charge.                                                                                                            |
| [**\_appareil EC \_ perdu**](ec-device-lost.md)                              | Un appareil Plug-and-Play a été supprimé ou est à nouveau disponible.                                                         |
| [**\_affichage EC \_ modifié**](ec-display-changed.md)                      | Le mode d’affichage a changé.                                                                                             |
| [**\_fin \_ de \_ segment ce**](ec-end-of-segment.md)                       | La fin d’un segment a été atteinte.                                                                                    |
| [**CE \_ EOS \_ bientôt**](ec-eos-soon.md)                                    | Non pris en charge.                                                                                                            |
| [**\_erreur EC \_ STILLPLAYING**](ec-error-stillplaying.md)                | Une commande asynchrone pour exécuter le graphique a échoué.                                                                      |
| [**\_ERRORABORT EC**](ec-errorabort.md)                                 | Une opération a été abandonnée en raison d’une erreur.                                                                             |
| [**\_ERRORABORTEX EC**](ec-errorabortex.md)                             | Une opération a été abandonnée en raison d’une erreur.                                                                             |
| [**\_modification du \_ mode \_ EXTDEVICE EC**](ec-extdevice-mode-change.md)         | Non pris en charge.                                                                                                            |
| [**\_fichier EC \_ fermé**](ec-file-closed.md)                              | Le fichier source a été fermé en raison d’un événement inattendu.                                                                |
| [**perte de la \_ fullscreen EC \_**](ec-fullscreen-lost.md)                      | Le convertisseur vidéo bascule en mode plein écran.                                                                  |
| [**\_graphe ce \_ modifié**](ec-graph-changed.md)                          | Le graphique de filtre a changé.                                                                                             |
| [**longueur des EC \_ \_ modifiés**](ec-length-changed.md)                        | La longueur d’une source a changé.                                                                                       |
| [**\_LOADSTATUS EC**](ec-loadstatus.md)                                 | Avertit l’application de la progression lors de l’ouverture d’un fichier réseau.                                                         |
| [**\_marquage EC \_ atteint**](ec-marker-hit.md)                                | Non pris en charge.                                                                                                            |
| [**redémarrage de l’EC \_ requis \_**](ec-need-restart.md)                            | Un filtre demande que le graphique soit redémarré.                                                                       |
| [**\_nouveau \_ code confidentiel ce**](ec-new-pin.md)                                      | Non pris en charge.                                                                                                            |
| [**\_fenêtre EC Notify \_**](ec-notify-window.md)                          | Avertit un filtre de la fenêtre du convertisseur vidéo.                                                                         |
| [**\_événement OLE \_ EC**](ec-ole-event.md)                                  | Un filtre transmet une chaîne de texte à l’application.                                                                     |
| [**\_fichier d’ouverture EC \_**](ec-opening-file.md)                            | Le graphique ouvre un fichier ou a fini d’ouvrir un fichier.                                                              |
| [**\_palette EC \_ modifiée**](ec-palette-changed.md)                      | La palette vidéo a changé.                                                                                            |
| [**en \_ Pause EC**](ec-paused.md)                                         | Une demande de suspension est terminée.                                                                                            |
| [**réouverture de la communauté \_ \_**](ec-please-reopen.md)                          | Le fichier source a changé.                                                                                              |
| [**\_prétraitement EC \_ terminé**](ec-preprocess-complete.md)              | Envoyé par le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) lorsqu’il termine le prétraitement pour l’encodage multipasse. |
| [**\_latence de traitement ce \_**](ec-processing-latency.md)                | Indique la durée pendant laquelle un composant prend le traitement de chaque échantillon.                                           |
| [**modification de la \_ qualité ce \_**](ec-quality-change.md)                        | Le graphique supprime des exemples, pour le contrôle de la qualité.                                                                       |
| [**\_rendu EC \_ terminé**](ec-render-finished.md)                      | Non pris en charge.                                                                                                            |
| [**redessin ce \_**](ec-repaint.md)                                       | Un convertisseur vidéo requiert un redessin.                                                                                      |
| [**latence de l' \_ exemple EC \_**](ec-sample-latency.md)                        | Spécifie la distance de planification d’un composant pour les exemples de traitement.                                                  |
| [**\_exemple EC \_ requis**](ec-sample-needed.md)                          | Demande un nouvel exemple d’entrée à partir du filtre de convertisseur vidéo amélioré (EVR).                                                |
| [**\_temps de nettoyage ce \_**](ec-scrub-time.md)                                | Spécifie l’horodatage de l’étape de Frame la plus récente.                                                                  |
| [**\_segment EC \_ démarré**](ec-segment-started.md)                      | Un nouveau segment a démarré.                                                                                                |
| [**arrêt de l’EC \_ \_**](ec-shutting-down.md)                          | Le graphique de filtre s’arrête, avant d’être détruit.                                                              |
| [**EC \_ SNDDEV \_ en \_ erreur**](ec-snddev-in-error.md)                     | Une erreur d’appareil s’est produite dans un filtre de capture audio.                                                                   |
| [**\_erreur de \_ sortie EC SNDDEV \_**](ec-snddev-out-error.md)                   | Une erreur d’appareil s’est produite dans un filtre de convertisseur audio.                                                                  |
| [**\_privation ce**](ec-starvation.md)                                 | Un filtre ne reçoit pas suffisamment de données.                                                                                    |
| [**\_changement d’État EC \_**](ec-state-change.md)                            | Le graphique de filtre a changé d’État.                                                                                       |
| [**État de l’UE \_**](ec-status.md)                                         | Contient deux chaînes d’État arbitraires.                                                                                    |
| [**\_étape EC \_ terminée**](ec-step-complete.md)                          | Un filtre effectuant l’exécution pas à pas du frame a effectué un pas à pas le nombre spécifié de frames.                                            |
| [**\_le contrôle de flux EC \_ \_ a démarré**](ec-stream-control-started.md)       | Une commande de démarrage de flux de contrôle a pris effet.                                                                          |
| [**\_le contrôle de flux EC s' \_ \_ est arrêté**](ec-stream-control-stopped.md)       | Une commande d’arrêt de contrôle de flux a pris effet.                                                                           |
| [**\_erreur de flux EC \_ \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | Une erreur s’est produite dans un flux. Le flux est toujours en cours d’exécution.                                                           |
| [**\_erreur de flux EC \_ \_ arrêtée**](ec-stream-error-stopped.md)           | Un flux s’est arrêté en raison d’une erreur.                                                                                 |
| [**\_code temporel EC \_ disponible**](ec-timecode-available.md)                | Non pris en charge.                                                                                                            |
| [**EC n’a pas été \_ généré**](ec-unbuilt.md)                                       | Envoyer par le contrôle Video lorsqu’un graphique a été détruit. Non transmis aux applications.                                 |
| [**\_USERABORT EC**](ec-userabort.md)                                   | L’utilisateur a terminé la lecture.                                                                                         |
| [**taille de la \_ vidéo ce \_ \_ modifiée**](ec-video-size-changed.md)               | La taille de la vidéo native a changé.                                                                                        |
| [**\_VIDEOFRAMEREADY EC**](ec-videoframeready.md)                       | Une image vidéo est prête à être affichée.                                                                                       |
| [**échec de la \_ \_ reconnexion EC VMR \_**](ec-vmr-reconnection-failed.md)     | Envoyé par VMR-7 et VMR-9 lorsqu’il n’a pas pu accepter une demande de modification de format dynamique du décodeur en amont.   |
| [**\_ \_ jeu RENDERDEVICE EC \_ VMR**](ec-vmr-renderdevice-set.md)           | Envoyé lorsque VMR a sélectionné son mécanisme de rendu.                                                                   |
| [**\_surface EC \_ VMR \_ retournée**](ec-vmr-surface-flipped.md)             | Envoyé lorsque l’exlocateur VMR-7's a appelé la méthode de retournement DirectDraw sur la surface qui est présentée.           |
| [**\_fenêtre EC \_ détruite**](ec-window-destroyed.md)                    | Le convertisseur vidéo a été détruit ou supprimé du graphique.                                                               |
| [**\_événement EC WMT \_**](ec-wmt-event.md)                                  | Envoyé par le filtre de lecteur ASF WM lorsqu’il lit des fichiers ASF protégés par la gestion des droits numériques (DRM).                    |
| [**événement d’index de l’WMT de la EC \_ \_ \_**](ec-wmt-index-event.md)                     | Envoyé lorsqu’une application utilise le writer ASF pour indexer les fichiers Windows Media Video.                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



