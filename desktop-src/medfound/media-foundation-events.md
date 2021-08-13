---
description: Événements de Media Foundation
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Événements de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a922127941bd94103eac9cfb02ef33d1c0b789eb632f2689a3adc81494c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268819"
---
# <a name="media-foundation-events"></a>Événements de Media Foundation



| Événement                                                                                        | Description                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Le périphérique audio a été supprimé.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | la session audio a été déconnectée d’une session de Services Terminal Windows                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | La session audio a été préemptée par une connexion en mode exclusif.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | Le format audio par défaut du périphérique audio a changé.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Paramètres de regroupement modifiés pour la session audio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | L’icône de session audio a changé.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | Le nom d’affichage de la session audio a changé.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | le système du serveur audio Windows a été arrêté.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | Le volume ou l’État muet de la session audio a changé                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Une source de média a commencé à mettre les données en mémoire tampon.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Une source de média A arrêté la mise en mémoire tampon des données.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | L’appareil a été supprimé.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | la session audio est déconnectée, car l’utilisateur s’est déconnecté d’une session des Services de Terminal Windows (WTS).                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | L’utilisateur a ouvert un flux audio en mode exclusif.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | Le format audio a changé.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | Arrêt du serveur de session audio.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | Le volume a changé.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | La source réseau a fini d’ouvrir une URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | La source réseau a démarré l’ouverture d’une URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | La configuration a été modifiée pour un schéma de protection de sortie.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | L’action d’un objet d’activation du contenu est terminée.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Signale la progression d’un objet activateur de contenu.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Déclenché par une source de média lorsqu’une présentation se termine.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Déclenché par la source de Sequencer lorsqu’un segment est terminé et qu’il est suivi d’un autre segment.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Déclenché par un flux de média lorsque le flux se termine.                                                                                                           |
| [MEError](meerror.md)                                                                       | Signale une erreur grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Type d’événement personnalisé.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | L’individualisation est terminée.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | L’individualisation est sur le début.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | L’acquisition de licence est terminée.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | L’acquisition de licence va commencer.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Déclenché lorsqu’un flux multimédia remet un nouvel exemple.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Déclenché par une source de média une nouvelle présentation est prête.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Déclenché par une source de média lorsqu’elle démarre un nouveau flux.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Une erreur récupérable s’est produite lors de la diffusion en continu.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | La stratégie de sortie pour un flux a changé.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Déclenché par une sortie approuvée si une erreur se produit lors de l’application de la stratégie de sortie.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contient des informations d’État sur l’application d’une stratégie de sortie.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | La méthode [**IMFOutputTrustAuthority :: SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) s’est terminée.                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Fournit des commentaires sur la qualité de la lecture au gestionnaire de qualité.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Déclenché par une source de média à la fin d’une tentative de reconnexion.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Déclenché par une source de média au début d’une tentative de reconnexion.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Déclenché par le convertisseur vidéo amélioré (EVR) lorsqu’il reçoit un événement utilisateur du présentateur.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Déclenché par la source de Sequencer lorsque la méthode [**IMFSequencerSource :: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) se termine de façon asynchrone. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Déclenché par la session multimédia lorsque les fonctionnalités de session changent.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Déclenché lorsque la méthode [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se termine de façon asynchrone.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Déclenché par la session multimédia lorsqu’elle a fini de lire la dernière présentation dans la file d’attente de lecture.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Déclenché par la session multimédia au démarrage d’une nouvelle présentation.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Déclenché lorsque la méthode [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) se termine de façon asynchrone.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Déclenché par la session multimédia lorsque la vitesse de lecture change.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Déclenché par la session multimédia lorsqu’elle termine une demande de nettoyage.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Déclenché lorsque la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se termine de façon asynchrone.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Déclenché lorsque la méthode [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) se termine de façon asynchrone.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Déclenché par la session multimédia lorsque le format change sur un récepteur multimédia.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Déclenché par la session multimédia lorsque la méthode [**IMFMediaSession :: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se termine de façon asynchrone.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Déclenché après la fin asynchrone de la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Déclenché par la session multimédia lorsque l’état d’une topologie change.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Déclenché lorsqu’un récepteur multimédia devient non valide.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Déclenché par une source de média lorsque les caractéristiques de la source changent.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Déclenché par une source de média lors de la mise à jour de ses métadonnées.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Déclenché par une source de média lorsque la méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se termine de façon asynchrone.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Déclenché par une source de média lorsque la vitesse de lecture change.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Déclenché par une source de média pour demander un nouveau taux de lecture.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Déclenché quand une source multimédia cherche à une nouvelle position.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Déclenché quand une source de média démarre sans rechercher.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Déclenché par une source de média lorsque la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se termine de façon asynchrone.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Déclenché par un flux multimédia lorsque le type de média du flux change.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Déclenché par un flux de média lorsque la méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se termine de façon asynchrone.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Déclenché par un flux de média après un appel à [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoque une recherche dans le flux.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Déclenché par les récepteurs de flux du EVR si le périphérique vidéo change.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Déclenché par un récepteur de flux lorsque le type de média du récepteur n’est plus valide.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Déclenché par un récepteur de flux après l’appel de la méthode [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état suspendu.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Déclenché par un récepteur de flux lorsque le flux a reçu suffisamment de données de préroll pour commencer le rendu.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Déclenché par un récepteur de flux lorsque le taux a changé.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Déclenché par un récepteur de flux pour demander un nouvel échantillon de média à partir du pipeline.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Déclenché par un récepteur de flux lorsqu’il termine une demande de nettoyage.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Déclenché par un récepteur de flux lorsqu’il termine la transition à l’État en cours d’exécution.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Déclenché par un récepteur de flux lorsqu’il termine la transition à l’état arrêté.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Déclenché par un flux de média lorsque la source démarre sans recherche.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Déclenché par un flux de média lorsque la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) se termine de façon asynchrone.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Signale qu’un flux multimédia n’a pas de données disponibles à une heure spécifiée.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Envoyé par une transformation de Media Foundation asynchrone (MFT) lorsqu’une opération de drainage est terminée.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Envoyé par une table MFT asynchrone quand de nouvelles données de sortie sont disponibles à partir de la table MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Envoyé par une table MFT asynchrone en réponse à un message de [**\_ marque de \_ commande \_ de message MFT**](mft-message-command-marker.md) .                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Envoyé par une table MFT asynchrone pour demander un nouvel exemple d’entrée.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Type d’événement inconnu.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Déclenché par une source de média lors du redémarrage ou de la recherche d’un flux déjà actif.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | L’appareil a été devancé.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | L’appareil a été supprimé.                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de programmation Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Générateurs d’événements de média](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



