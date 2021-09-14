---
description: dans Windows 7, les api de plateforme de haut niveau qui utilisent des api Audio de base, telles que les api Media Foundation, DirectSound et Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison Audio par défaut.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtention du point de terminaison de l’appareil pour le routage du flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114926"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Obtention du point de terminaison de l’appareil pour le routage du flux

dans Windows 7, les api de plateforme de haut niveau qui utilisent des api Audio de base, telles que les api Media Foundation, DirectSound et Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison Audio par défaut. Les applications multimédias qui utilisent ces API (par exemple, une application activant un objet **IDirectSound** ou **IBaseFilter** sur un objet [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) utilisent le comportement de routage de flux sans aucune modification de la source.

Les API de haut niveau implémentent le routage de flux pour le point de terminaison d’appareil obtenu par le biais de [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si une application est diffusée sur l’appareil par défaut, la fonctionnalité de routage de flux fonctionne comme défini. les Flux ne sont pas basculés vers le nouvel appareil s’ils sont récupérés par un autre mécanisme, même s’ils sont identiques à ceux du périphérique par défaut.

Une application multimédia qui utilise des API audio de base directement (client WASAPI) peut fournir une implémentation de routage de flux personnalisée pour tout périphérique de rendu ou de capture. Un client WASAPI peut répliquer le implémentation fourni par les API de haut niveau en le limitant aux flux ouverts sur les appareils qui sont définis en tant qu’appareil par défaut. Pour obtenir une référence au point de terminaison de l’appareil par défaut, le client doit appeler [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Dans cet appel, le client doit indiquer s’il requiert un pointeur vers le périphérique de rendu par défaut ou l’appareil de capture par défaut en spécifiant le paramètre de *flux* de données. Le client doit également spécifier le rôle approprié pour le point de terminaison dans l’attribut **ERole** (**eConsole** ou **eCommunications**). N’utilisez pas **eMultimedia**.

Si l’application est diffusée sur un autre appareil, l’application peut l’extraire en spécifiant une chaîne d’ID de point de terminaison (en appelant [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Une fois l’appareil identifié, le client WASAPI peut fournir l’implémentation du routage de flux en gérant les notifications d’appareil et de session audio envoyées pour l’appareil. Pour plus d’informations sur ces notifications, consultez [notifications pertinentes pour le routage de flux](relevant-device-notifications-for-stream-routing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API MMDevice](mmdevice-api.md)
</dt> <dt>

[À propos de WASAPI](wasapi.md)
</dt> <dt>

[Routage de flux](stream-routing.md)
</dt> </dl>

 

 



