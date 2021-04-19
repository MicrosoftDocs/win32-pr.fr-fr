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
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="20b77-103">Constantes d’événement (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="20b77-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="20b77-104">Les appareils mobiles Windows définissent les valeurs d’événement suivantes.</span><span class="sxs-lookup"><span data-stu-id="20b77-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="20b77-105">Constante</span><span class="sxs-lookup"><span data-stu-id="20b77-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="20b77-106">Description</span><span class="sxs-lookup"><span data-stu-id="20b77-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="20b77-107"><dt>**fonctionnalités de l' \_ appareil d’événements wpd \_ \_ \_ mises à jour**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="20b77-108">Cet événement indique que les fonctionnalités de l’appareil ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="20b77-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="20b77-109">Les clients doivent redemander l’appareil s’ils ont pris des décisions en fonction des fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="20b77-110"><dt>**\_appareil d’événement wpd \_ \_ supprimé**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="20b77-111">Cet événement est envoyé lorsqu’un pilote d’appareil est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="20b77-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="20b77-112">En général, cela est dû au fait que l’appareil est débranché.</span><span class="sxs-lookup"><span data-stu-id="20b77-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="20b77-113">Les clients doivent libérer l’interface **IPortableDevice** et toutes les interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) spécifiées dans le **paramètre d’événement wpd ID de l' \_ \_ \_ \_ appareil \_ PNP**.</span><span class="sxs-lookup"><span data-stu-id="20b77-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="20b77-114"><dt>**réinitialisation de l' \_ appareil d’événements wpd \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="20b77-115">Cet événement indique que l’appareil va être réinitialisé et que tous les clients connectés doivent fermer leurs connexions à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="20b77-116"><dt>**\_objet d’événement wpd \_ \_ ajouté**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="20b77-117">Cet événement indique qu’un nouvel objet est disponible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="20b77-118"><dt>**\_objet d’événement wpd \_ \_ supprimé**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="20b77-119">Cet événement est envoyé une fois qu’un objet précédemment existant a été supprimé de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="20b77-120">L’objet peut être un objet de contenu, par exemple, un fichier image a été supprimé ; Il peut également s’agir d’un objet fonctionnel, par exemple, un nouveau périphérique de stockage a été débranché de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="20b77-121"><dt>**transfert de l' \_ objet d’événement wpd \_ \_ \_ demandé**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="20b77-122">Cet événement est envoyé pour demander à une application de transférer un objet particulier à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20b77-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="20b77-123">L’objet est généralement un objet de contenu, par exemple, un fichier image.</span><span class="sxs-lookup"><span data-stu-id="20b77-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="20b77-124"><dt>**\_objet d’événement wpd \_ \_ mis à jour**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="20b77-125">Cet événement est envoyé une fois qu’un objet a été mis à jour et que n’importe quel client connecté doit actualiser sa vue de cet objet.</span><span class="sxs-lookup"><span data-stu-id="20b77-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="20b77-126"><dt>**\_méthode du service d’événements wpd \_ \_ \_ terminée**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="20b77-127">Cet événement est envoyé lorsqu’un pilote a terminé l’appel d’une méthode de service.</span><span class="sxs-lookup"><span data-stu-id="20b77-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="20b77-128">Cet événement doit être envoyé même lorsque la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="20b77-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="20b77-129">Il s’agit d’un événement DDI WPD interne qui n’est pas disponible pour les applications via [**IPortableDevice :: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) ou [**IPortableDeviceService :: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span><span class="sxs-lookup"><span data-stu-id="20b77-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="20b77-130"><dt>**\_format de \_ stockage des événements wpd \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="20b77-131">Cet événement indique la progression d’une opération de format sur un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="20b77-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="20b77-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20b77-132">Requirements</span></span>



| <span data-ttu-id="20b77-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20b77-133">Requirement</span></span> | <span data-ttu-id="20b77-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="20b77-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b77-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="20b77-135">Header</span></span><br/> | <dl> <span data-ttu-id="20b77-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b77-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20b77-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20b77-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b77-138">Constantes</span><span class="sxs-lookup"><span data-stu-id="20b77-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




