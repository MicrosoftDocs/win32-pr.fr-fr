---
title: Interfaces de diffusion multimédia en continu
description: L’API de diffusion multimédia en continu fournit les interfaces suivantes.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6cdb1893af3170ae9ec5989498a007230992361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196756"
---
# <a name="media-streaming-interfaces"></a>Interfaces de diffusion multimédia en continu

L' [API de diffusion multimédia en continu](media-streaming-api-portal.md) fournit les interfaces suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                 | Description                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Représente un [**IBasicDevice**](ibasicdevice.md) actif qui est associé à un périphérique UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Fournit des méthodes statiques pour créer des objets [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) . <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Encapsule les méthodes et les événements nécessaires pour modéliser un appareil DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Encapsule les méthodes et les événements nécessaires pour récupérer une liste de convertisseurs multimédias numériques mis en cache (DMRs) et/ou de serveurs multimédias numériques (DMSs), ou pour rechercher de manière asynchrone le DMRs et/ou DMSs actuellement sur le réseau.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Encapsule les méthodes nécessaires pour fournir des informations sur l’icône d’un appareil DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Représente une paire d’objets [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) qui est constituée d’un convertisseur et d’un serveur.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Encapsule les méthodes et les événements nécessaires pour représenter un appareil de convertisseur de médias numériques DLNA (DMR).<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Encapsule les méthodes nécessaires pour fournir des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Encapsule les méthodes nécessaires pour créer de manière asynchrone une nouvelle instance d’un objet qui implémente l’interface [**IMediaRenderer**](imediarenderer.md) .<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Encapsule les méthodes nécessaires pour sélectionner un flux de manière asynchrone.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Encapsule les méthodes nécessaires pour fournir des informations sur les paramètres de transport actuels du DMR. Ces paramètres incluent l’état du transport actuel et des informations sur les méthodes qui peuvent être appelées actuellement sur le DMR.<br/> |



 

 

