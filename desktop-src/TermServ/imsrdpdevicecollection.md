---
title: Interface IMsRdpDeviceCollection
description: Représente une collection d’objets périphériques.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383883"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="8253c-105">Interface IMsRdpDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="8253c-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="8253c-106">Représente une collection d’objets périphériques.</span><span class="sxs-lookup"><span data-stu-id="8253c-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="8253c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8253c-107">Members</span></span>

<span data-ttu-id="8253c-108">L’interface **IMsRdpDeviceCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8253c-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8253c-109">**IMsRdpDeviceCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8253c-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8253c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8253c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8253c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8253c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8253c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8253c-112">Methods</span></span>

<span data-ttu-id="8253c-113">L’interface **IMsRdpDeviceCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8253c-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="8253c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="8253c-114">Method</span></span>                                                        | <span data-ttu-id="8253c-115">Description</span><span class="sxs-lookup"><span data-stu-id="8253c-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="8253c-116">**RescanDevices**</span><span class="sxs-lookup"><span data-stu-id="8253c-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="8253c-117">Actualise la liste des objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8253c-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8253c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8253c-118">Properties</span></span>

<span data-ttu-id="8253c-119">L’interface **IMsRdpDeviceCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8253c-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="8253c-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="8253c-120">Property</span></span>                                                                 | <span data-ttu-id="8253c-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8253c-121">Access type</span></span>          | <span data-ttu-id="8253c-122">Description</span><span class="sxs-lookup"><span data-stu-id="8253c-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="8253c-123">**DeviceById**</span><span class="sxs-lookup"><span data-stu-id="8253c-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="8253c-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8253c-124">Read-only</span></span><br/> | <span data-ttu-id="8253c-125">Récupère l’appareil avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="8253c-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="8253c-126">**DeviceByIndex**</span><span class="sxs-lookup"><span data-stu-id="8253c-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="8253c-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8253c-127">Read-only</span></span><br/> | <span data-ttu-id="8253c-128">Récupère l’appareil au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8253c-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="8253c-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="8253c-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="8253c-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8253c-130">Read-only</span></span><br/> | <span data-ttu-id="8253c-131">Récupère le nombre d’objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8253c-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="8253c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8253c-132">Requirements</span></span>



| <span data-ttu-id="8253c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8253c-133">Requirement</span></span> | <span data-ttu-id="8253c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8253c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8253c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8253c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8253c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8253c-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="8253c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8253c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8253c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8253c-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8253c-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8253c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="8253c-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8253c-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="8253c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8253c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8253c-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8253c-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="8253c-143">IID</span><span class="sxs-lookup"><span data-stu-id="8253c-143">IID</span></span><br/>                      | <span data-ttu-id="8253c-144">IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="8253c-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8253c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8253c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8253c-146">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="8253c-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="8253c-147">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="8253c-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

