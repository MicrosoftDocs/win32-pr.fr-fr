---
title: Interface IMsRdpDevice
description: Contient des informations sur un objet appareil.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, Description
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512788"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="73ae8-105">Interface IMsRdpDevice</span><span class="sxs-lookup"><span data-stu-id="73ae8-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="73ae8-106">Contient des informations sur un objet appareil.</span><span class="sxs-lookup"><span data-stu-id="73ae8-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="73ae8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="73ae8-107">Members</span></span>

<span data-ttu-id="73ae8-108">L’interface **IMsRdpDevice** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="73ae8-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73ae8-109">**IMsRdpDevice** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73ae8-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="73ae8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73ae8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73ae8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73ae8-111">Properties</span></span>

<span data-ttu-id="73ae8-112">L’interface **IMsRdpDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="73ae8-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="73ae8-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="73ae8-113">Property</span></span>                                                               | <span data-ttu-id="73ae8-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="73ae8-114">Access type</span></span>           | <span data-ttu-id="73ae8-115">Description</span><span class="sxs-lookup"><span data-stu-id="73ae8-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ae8-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="73ae8-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="73ae8-117">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73ae8-117">Read-only</span></span><br/>  | <span data-ttu-id="73ae8-118">Récupère la description de l’appareil à afficher à l’utilisateur si le nom complet n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="73ae8-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="73ae8-119">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="73ae8-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="73ae8-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73ae8-120">Read-only</span></span><br/>  | <span data-ttu-id="73ae8-121">Récupère l’identificateur d’instance d’appareil de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73ae8-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="73ae8-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="73ae8-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="73ae8-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73ae8-123">Read-only</span></span><br/>  | <span data-ttu-id="73ae8-124">Récupère le nom complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73ae8-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="73ae8-125">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="73ae8-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="73ae8-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="73ae8-126">Read/write</span></span><br/> | <span data-ttu-id="73ae8-127">Indique l’état de redirection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73ae8-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="73ae8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73ae8-128">Requirements</span></span>



| <span data-ttu-id="73ae8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73ae8-129">Requirement</span></span> | <span data-ttu-id="73ae8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="73ae8-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ae8-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73ae8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73ae8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73ae8-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="73ae8-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73ae8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73ae8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73ae8-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="73ae8-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="73ae8-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="73ae8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="73ae8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="73ae8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ae8-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="73ae8-139">IID</span><span class="sxs-lookup"><span data-stu-id="73ae8-139">IID</span></span><br/>                      | <span data-ttu-id="73ae8-140">IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="73ae8-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="73ae8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73ae8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ae8-142">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="73ae8-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="73ae8-143">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="73ae8-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

