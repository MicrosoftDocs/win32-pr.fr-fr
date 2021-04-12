---
title: Informations de référence sur l’API point de contrôle
description: Les interfaces suivantes font partie de l’API de point de contrôle avec la technologie UPnP. L’API du point de contrôle prend en charge Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic et C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309697"
---
# <a name="control-point-api-reference"></a>Informations de référence sur l’API point de contrôle

Les interfaces suivantes font partie de l’API de point de contrôle avec la technologie UPnP. L’API du point de contrôle prend en charge Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic et C++.



| Interface                                                                                      | Description                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Permet à une application d’accéder à l’indicateur de famille d’adresses de l’objet de recherche d’appareil.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Permet à une application de charger une description d’appareil. Cette interface est sécurisée pour les scripts.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Permet à une application de recevoir les résultats d’une opération de chargement asynchrone.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Permet à une application de récupérer des informations sur un appareil spécifique.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Permet à une application d’obtenir l’URL d’un document de description de l’appareil.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Fournit une méthode pour obtenir l’intégralité du document de description de l’appareil XML pour un appareil spécifique.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Permet à une application de trouver un appareil.                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Permet à une application de recevoir des résultats de recherche asynchrones à partir de l’infrastructure UPnP avec le GUID de la carte réseau par le biais duquel la publication de l’appareil a été reçue.                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Permet à une application de recevoir des résultats de recherche asynchrones à partir de l’infrastructure UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Énumère une collection d’appareils.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Permet à une application de définir des en-têtes HTTP « agent utilisateur » à partir d’instances de classe qui implémentent les interfaces [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ou [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Permet à une application de récupérer des informations d’État et d’appeler des actions pour un service.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Interroger de manière asynchrone des variables d’État et appeler des actions sur une instance d’un service.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Permet à une application de recevoir une notification de l’infrastructure UPnP lorsque des événements se produisent.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Énumère une collection de services.                                                                                                                                                                                           |



 

 

 




