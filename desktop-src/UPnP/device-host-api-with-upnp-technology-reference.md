---
title: Informations de référence sur l’API d’hôte d’appareil
description: Les interfaces suivantes font partie de l’API de l’hôte d’appareil avec la technologie UPnP. L’hôte d’appareil avec la technologie UPnP prend en charge Microsoft Visual Basic et C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380190"
---
# <a name="device-host-api-reference"></a>Informations de référence sur l’API d’hôte d’appareil

Les interfaces suivantes font partie de l’API de l’hôte d’appareil avec la technologie UPnP. L’hôte d’appareil avec la technologie UPnP prend en charge Microsoft Visual Basic et C++.

Cette API ne prend pas en charge Microsoft Visual Basic Scripting Edition (VBScript).



| Interface                                                  | Description                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | Utilisé par l’hôte d’appareil pour gérer les appareils et les services associés.                                     |
| [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | Utilisé par l’hôte d’appareil pour démarrer et arrêter des fournisseurs de périphériques.                                         |
| [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | Utilisé par les appareils pour envoyer des notifications d’événements à l’hôte de l’appareil.                                     |
| [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | Utilisé par l’hôte d’appareil pour s’abonner ou annuler l’abonnement aux événements fournis par le service hébergé.       |
| [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | Utilisé par les appareils pour s’inscrire auprès de l’hôte de l’appareil.                                                   |
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | Utilisé par les appareils pour obtenir des informations sur un demandeur (c’est-à-dire un point de contrôle) et la demande. |
| [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | Utilisé par les appareils pour s’inscrire à nouveau auprès de l’hôte de l’appareil.                                                |



 

 

 




