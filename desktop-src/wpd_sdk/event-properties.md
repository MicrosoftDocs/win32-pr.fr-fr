---
description: Appareils mobiles Windows prend en charge les propriétés d’événement suivantes.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propriétés de l’événement (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537701"
---
# <a name="event-properties"></a><span data-ttu-id="2c1a8-103">Propriétés de l’événement</span><span class="sxs-lookup"><span data-stu-id="2c1a8-103">Event Properties</span></span>

<span data-ttu-id="2c1a8-104">Appareils mobiles Windows prend en charge les propriétés d’événement suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2c1a8-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="2c1a8-105">Property</span></span></th>
<th><span data-ttu-id="2c1a8-106">VarType</span><span class="sxs-lookup"><span data-stu-id="2c1a8-106">VarType</span></span></th>
<th><span data-ttu-id="2c1a8-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c1a8-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c1a8-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="2c1a8-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="2c1a8-110">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c1a8-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="2c1a8-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="2c1a8-113">Valeur booléenne qui spécifie si l’événement est diffusé à tous les clients. Les clients peuvent recevoir cet événement en inscrivant leur rappel avec <strong>IPortableDevice :: Advise</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c1a8-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="2c1a8-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="2c1a8-116">Valeur booléenne qui spécifie si la hiérarchie enfant de l’objet a changé. Ce paramètre est utilisé pour informer l’appelant que certains enfants de l’objet spécifié ont été ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="2c1a8-117">En général, la modification de la hiérarchie est lancée côté appareil.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="2c1a8-118">Les clients devront peut-être réénumérer les enfants de ce dossier pour maintenir à jour leurs vues.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c1a8-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="2c1a8-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="2c1a8-121">Valeur qui identifie un événement.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c1a8-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="2c1a8-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="2c1a8-124">Le cookie est remis à un client lorsqu’il demande la création d’un objet en appelant la méthode <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent :: CreateObjectWithPropertiesAndData</strong></a> . Ce paramètre est ajouté pour aider l’appelant à lier un événement ajouté à l’objet à la demande qu’il a envoyée pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="2c1a8-125">Le pilote rétablit ce cookie comme valeur de retour <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> lors du traitement de la commande <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .</span><span class="sxs-lookup"><span data-stu-id="2c1a8-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c1a8-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="2c1a8-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="2c1a8-128">Valeur qui identifie de façon unique l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="2c1a8-129">Cette propriété est similaire à <strong>WPD_OBJECT_PARENT_ID</strong>, mais cet ID ne change pas entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c1a8-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="2c1a8-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="2c1a8-132">Valeur qui spécifie la progression d’une opération en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="2c1a8-133">La valeur de cette propriété peut être comprise entre 0 et 100, avec 100 indiquant que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c1a8-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="2c1a8-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="2c1a8-136">Valeur qui indique l’état actuel de l’opération, par exemple, démarrée, en cours d’exécution, arrêtée, etc. Les valeurs possibles de ce paramètre proviennent de l’énumération <strong>WPD_OPERATION_STATES</strong> définie dans PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="2c1a8-137">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c1a8-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="2c1a8-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="2c1a8-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="2c1a8-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="2c1a8-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="2c1a8-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="2c1a8-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="2c1a8-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c1a8-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="2c1a8-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="2c1a8-147">Valeur qui spécifie le périphérique à l’origine de l’événement. Il s’agit de l’identificateur de périphérique ou de service fourni par le système plug-and-Play (PnP). il s’agit de la même chaîne que celle utilisée dans les méthodes <strong>IPortableDevice :: Open</strong>ou <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService :: Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2c1a8-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c1a8-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="2c1a8-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="2c1a8-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="2c1a8-150">Chaîne utilisée par un pilote WPD pour identifier l’opération d’une méthode de service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="2c1a8-151">Les applications ne doivent pas utiliser ce paramètre directement.</span><span class="sxs-lookup"><span data-stu-id="2c1a8-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2c1a8-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c1a8-152">Requirements</span></span>



| <span data-ttu-id="2c1a8-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c1a8-153">Requirement</span></span> | <span data-ttu-id="2c1a8-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c1a8-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1a8-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c1a8-155">Header</span></span><br/> | <dl> <span data-ttu-id="2c1a8-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c1a8-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1a8-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c1a8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1a8-158">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="2c1a8-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




