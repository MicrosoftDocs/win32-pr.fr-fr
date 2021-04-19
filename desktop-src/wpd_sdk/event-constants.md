---
description: Les appareils mobiles Windows définissent les valeurs d’événement suivantes.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes d’événement (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542611"
---
# <a name="event-constants-portabledeviceh"></a>Constantes d’événement (PortableDevice. h)

Les appareils mobiles Windows définissent les valeurs d’événement suivantes.



| Constante                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**fonctionnalités de l' \_ appareil d’événements wpd \_ \_ \_ mises à jour**</dt> </dl> | Cet événement indique que les fonctionnalités de l’appareil ont été modifiées. Les clients doivent redemander l’appareil s’ils ont pris des décisions en fonction des fonctionnalités de l’appareil.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_appareil d’événement wpd \_ \_ supprimé**</dt> </dl>                                         | Cet événement est envoyé lorsqu’un pilote d’appareil est en cours de déchargement. En général, cela est dû au fait que l’appareil est débranché.<br/> Les clients doivent libérer l’interface **IPortableDevice** et toutes les interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) spécifiées dans le **paramètre d’événement wpd ID de l' \_ \_ \_ \_ appareil \_ PNP**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**réinitialisation de l' \_ appareil d’événements wpd \_ \_**</dt> </dl>                                               | Cet événement indique que l’appareil va être réinitialisé et que tous les clients connectés doivent fermer leurs connexions à l’appareil.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_objet d’événement wpd \_ \_ ajouté**</dt> </dl>                                               | Cet événement indique qu’un nouvel objet est disponible sur l’appareil.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_objet d’événement wpd \_ \_ supprimé**</dt> </dl>                                         | Cet événement est envoyé une fois qu’un objet précédemment existant a été supprimé de l’appareil.<br/> L’objet peut être un objet de contenu, par exemple, un fichier image a été supprimé ; Il peut également s’agir d’un objet fonctionnel, par exemple, un nouveau périphérique de stockage a été débranché de l’appareil.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**transfert de l' \_ objet d’événement wpd \_ \_ \_ demandé**</dt> </dl>       | Cet événement est envoyé pour demander à une application de transférer un objet particulier à partir de l’appareil.<br/> L’objet est généralement un objet de contenu, par exemple, un fichier image.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_objet d’événement wpd \_ \_ mis à jour**</dt> </dl>                                         | Cet événement est envoyé une fois qu’un objet a été mis à jour et que n’importe quel client connecté doit actualiser sa vue de cet objet.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_méthode du service d’événements wpd \_ \_ \_ terminée**</dt> </dl>             | Cet événement est envoyé lorsqu’un pilote a terminé l’appel d’une méthode de service. Cet événement doit être envoyé même lorsque la méthode échoue. Il s’agit d’un événement DDI WPD interne qui n’est pas disponible pour les applications via [**IPortableDevice :: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) ou [**IPortableDeviceService :: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_format de \_ stockage des événements wpd \_**</dt> </dl>                                         | Cet événement indique la progression d’une opération de format sur un objet de stockage.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> </dl>

 

 




