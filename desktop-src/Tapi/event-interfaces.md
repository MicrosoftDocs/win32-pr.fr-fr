---
description: Les interfaces d’événement (notification) permettent à une application TAPI 3 de répondre aux événements asynchrones.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfaces d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a4ecf097d761e98b723b37d9de6adcfd7ebb60696ce5e389426965534d63f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660839"
---
# <a name="event-interfaces"></a>Interfaces d’événements

Les interfaces d’événement (notification) permettent à une application TAPI 3 de répondre aux événements asynchrones.

Vous devez appeler la méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) et définir un masque de filtre d’événement pour activer la réception des événements de demande. Si vous n’appelez pas **ITTAPI ::p ut \_ EventFilter**, votre application ne recevra aucun événement.

Consultez la vue d’ensemble des [événements](./asynchronous-spontaneous-events.md) pour obtenir une description de la façon dont une application garantit la réception des notifications. Pour plus d’informations sur la définition d’un masque de filtre pour des types d’événements individuels, consultez les interfaces individuelles figurant dans le tableau suivant.



| Interface                                                           | Description                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Récupère la description des événements d’adresse.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Récupère la description des événements de terminal de reconnaissance vocale automatique.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Récupère la description des événements CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Récupère la description des événements de modification des informations sur les appels.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Récupère la description des événements de média d’appel.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Récupère la description des événements de notification d’appel.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Récupère la description des événements d’état d’appel.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Récupère des informations sur les événements DTMF digit pendant un appel.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Récupère des informations sur les appels qui requièrent la génération de chiffres DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Récupère les données relatives à la demande de collecte des chiffres d’une application.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Récupère la description des événements de terminal de fichier.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Récupère la description des événements participant à la Conférence.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Récupère la description des événements de téléphone.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Récupère la description des événements de qualité de service (QOS).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Récupère la description des événements de file d’attente ACD (Automatic Call distribution).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Récupère la description des événements de demande de [téléphonie assistée](./assisted-telephony-overview.md) .                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Récupère la description des événements d’objets TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Étend [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); Récupère un pointeur vers l’objet Phone qui a provoqué l’événement d’objet TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Récupère des informations sur un événement de détection de tonalité.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Récupère la description des événements de terminal de tonalité.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Récupère la description des événements de terminal de conversion de texte par synthèse vocale (TTS).                                                                          |



 



| Interface                                                                                             | Description                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Avertit les applications clientes des modifications apportées à un terminal enfichable.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Inscrit et annule l’inscription d’une application cliente à des fins de notification concernant les événements de terminal enfichables. |



 

 

 
