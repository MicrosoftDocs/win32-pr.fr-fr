---
title: Interface IBasicDevice
description: Encapsule les méthodes et les événements nécessaires pour modéliser un appareil DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API de diffusion multimédia en continu de l’interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, décrite
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412867"
---
# <a name="ibasicdevice-interface"></a>Interface IBasicDevice

Encapsule les méthodes et les événements nécessaires pour modéliser un appareil DLNA.

## <a name="members"></a>Membres

L’interface **IBasicDevice** hérite de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBasicDevice** possède ces méthodes.



| Méthode                                                                                 | Description                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Ajouter \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | Inscrit un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Récupère une valeur qui indique si l’appareil peut sortir de veille.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Retourne une valeur d’énumération indiquant si l’appareil est actuellement en ligne, hors ligne ou en veille, mais en éveil.<br/> |
| [**Description**](ibasicdevice-description.md)                                        | Récupère une description de l’appareil.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Récupère le nom convivial de l’appareil.<br/>                                                                               |
| [**Icônes**](ibasicdevice-icons.md)                                                    | Retourne un vecteur d’interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .<br/>                                                  |
| [**AdressesIP**](ibasicdevice-ipaddresses.md)                                        | Retourne un vecteur d’adresses IP.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Récupère le nom du fabricant de l’appareil.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Récupère l’URL du fabricant de l’appareil.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Récupère le nom du modèle de l’appareil.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Récupère le numéro de modèle de l’appareil.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Récupère l’URL du modèle de l’appareil.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Retourne un vecteur d’adresses physiques.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Récupère l’URL de présentation de l’appareil.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Retourne un vecteur d’URL de diffusion en continu à distance.<br/>                                                                          |
| [**supprimer \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Annule l’inscription d’un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | Récupère le numéro de série de l’appareil.<br/>                                                                               |
| [**Entrer**](ibasicdevice-type.md)                                                      | Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Récupère le nom d’appareil unique de l’appareil (UDN).<br/>                                                                    |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

