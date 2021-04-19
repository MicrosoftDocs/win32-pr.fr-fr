---
description: L’interface de l’appareil peut être décrite par une valeur GUID. Les appareils mobiles Windows définissent l’interface de périphérique suivante.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID de l’interface de l’appareil (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542402"
---
# <a name="device-interface-guids"></a>GUID de l’interface de l’appareil

L’interface de l’appareil peut être décrite par une valeur **GUID** . Les appareils mobiles Windows définissent l’interface de périphérique suivante.



| Constante                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ wpd**</dt> </dl>                          | Identifie les périphériques qui s’affichent dans une énumération WPD normale. Tout appareil qui inscrit ce GUID d’interface est énuméré quand une application appelle la méthode [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ wpd \_ privé**</dt> </dl> | Identifie les appareils qui n’apparaîtront pas au cours d’une énumération WPD normale. Tout appareil qui inscrit ce GUID d’interface est énuméré uniquement quand une application appelle la méthode [**IPortableDeviceManager :: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ du \_ service DEVINTERFACE wpd \_**</dt> </dl> | Dans Windows 7, les applications peuvent énumérer tous les services d’appareil WPD en appelant [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) et en utilisant cette classe d’interface comme GUID de type de service.<br/>                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Guide de référence de programmation](programming-reference.md)
</dt> </dl>

 

 




