---
title: Interface IMsRdpDeviceV2
description: Contient des informations sur un objet appareil. Il s’agit d’une amélioration de l’interface IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, Description
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509503"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="9ea23-106">Interface IMsRdpDeviceV2</span><span class="sxs-lookup"><span data-stu-id="9ea23-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="9ea23-107">Contient des informations sur un objet appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea23-107">Contains information about a device object.</span></span> <span data-ttu-id="9ea23-108">Il s’agit d’une amélioration de l’interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea23-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="9ea23-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9ea23-109">Members</span></span>

<span data-ttu-id="9ea23-110">L’interface **IMsRdpDeviceV2** hérite de [**IMsRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ea23-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="9ea23-111">**IMsRdpDeviceV2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ea23-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="9ea23-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ea23-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ea23-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9ea23-113">Properties</span></span>

<span data-ttu-id="9ea23-114">L’interface **IMsRdpDeviceV2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9ea23-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="9ea23-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="9ea23-115">Property</span></span>                                                                 | <span data-ttu-id="9ea23-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="9ea23-116">Access type</span></span>          | <span data-ttu-id="9ea23-117">Description</span><span class="sxs-lookup"><span data-stu-id="9ea23-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ea23-118">**CmClassGuid**</span><span class="sxs-lookup"><span data-stu-id="9ea23-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="9ea23-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-119">Read-only</span></span><br/> | <span data-ttu-id="9ea23-120">Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea23-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="9ea23-121">**CmDeviceInstance**</span><span class="sxs-lookup"><span data-stu-id="9ea23-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="9ea23-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-122">Read-only</span></span><br/> | <span data-ttu-id="9ea23-123">Contient l’instance d’appareil Configuration Manager de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea23-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="9ea23-124">**DeviceText**</span><span class="sxs-lookup"><span data-stu-id="9ea23-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="9ea23-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-125">Read-only</span></span><br/> | <span data-ttu-id="9ea23-126">Contient le texte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea23-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="9ea23-127">**DriveLetterBitmap**</span><span class="sxs-lookup"><span data-stu-id="9ea23-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="9ea23-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-128">Read-only</span></span><br/> | <span data-ttu-id="9ea23-129">Contient un champ de binaire qui représente une carte des lettres de lecteur contenues dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ea23-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="9ea23-130">**IsCompositeDevice**</span><span class="sxs-lookup"><span data-stu-id="9ea23-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="9ea23-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-131">Read-only</span></span><br/> | <span data-ttu-id="9ea23-132">Spécifie si l’appareil est un appareil composite.</span><span class="sxs-lookup"><span data-stu-id="9ea23-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="9ea23-133">**IsOptionalDevice**</span><span class="sxs-lookup"><span data-stu-id="9ea23-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="9ea23-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-134">Read-only</span></span><br/> | <span data-ttu-id="9ea23-135">Spécifie si l’appareil est facultatif pour la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="9ea23-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="9ea23-136">**IsUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="9ea23-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="9ea23-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9ea23-137">Read-only</span></span><br/> | <span data-ttu-id="9ea23-138">Spécifie si l’appareil est destiné à la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="9ea23-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="9ea23-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ea23-139">Requirements</span></span>



| <span data-ttu-id="9ea23-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ea23-140">Requirement</span></span> | <span data-ttu-id="9ea23-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ea23-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea23-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ea23-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9ea23-143">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="9ea23-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="9ea23-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ea23-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9ea23-145">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="9ea23-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="9ea23-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9ea23-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ea23-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ea23-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ea23-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9ea23-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ea23-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ea23-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9ea23-150">IID</span><span class="sxs-lookup"><span data-stu-id="9ea23-150">IID</span></span><br/>                      | <span data-ttu-id="9ea23-151">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="9ea23-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





