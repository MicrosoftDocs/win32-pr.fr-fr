---
title: Interface IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Définit la connexion d’un disque dur au sein de la machine virtuelle.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtual PC de l’interface IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518083"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="c8ea5-105">Interface IVMHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="c8ea5-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="c8ea5-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8ea5-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8ea5-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8ea5-108">Définit la connexion d’un disque dur au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="c8ea5-109">Un objet **IVMHardDiskConnection** est retourné à partir de la méthode [**IVMVirtualMachine :: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="c8ea5-110">Vous pouvez également récupérer un objet **IVMHardDiskConnection** à partir de l’objet [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c8ea5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c8ea5-111">Members</span></span>

<span data-ttu-id="c8ea5-112">L’interface **IVMHardDiskConnection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c8ea5-113">**IVMHardDiskConnection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8ea5-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="c8ea5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8ea5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8ea5-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8ea5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8ea5-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8ea5-116">Methods</span></span>

<span data-ttu-id="c8ea5-117">L’interface **IVMHardDiskConnection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="c8ea5-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="c8ea5-118">Method</span></span>                                                         | <span data-ttu-id="c8ea5-119">Description</span><span class="sxs-lookup"><span data-stu-id="c8ea5-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="c8ea5-120">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="c8ea5-121">Définit l’emplacement du bus auquel ce disque dur est attaché.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c8ea5-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8ea5-122">Properties</span></span>

<span data-ttu-id="c8ea5-123">L’interface **IVMHardDiskConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="c8ea5-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="c8ea5-124">Property</span></span>                                                              | <span data-ttu-id="c8ea5-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c8ea5-125">Access type</span></span>          | <span data-ttu-id="c8ea5-126">Description</span><span class="sxs-lookup"><span data-stu-id="c8ea5-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="c8ea5-127">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="c8ea5-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8ea5-128">Read-only</span></span><br/> | <span data-ttu-id="c8ea5-129">Numéro de bus auquel l’image de lecteur est attachée.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="c8ea5-130">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="c8ea5-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8ea5-131">Read-only</span></span><br/> | <span data-ttu-id="c8ea5-132">Numéro de l’appareil auquel l’image de lecteur est attachée.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="c8ea5-133">**Dur**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="c8ea5-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8ea5-134">Read-only</span></span><br/> | <span data-ttu-id="c8ea5-135">Objet de disque dur correspondant à cette connexion.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="c8ea5-136">**UndoHardDisk**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="c8ea5-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8ea5-137">Read-only</span></span><br/> | <span data-ttu-id="c8ea5-138">Objet de disque dur correspondant à l’image de disque d’annulation de cette connexion.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8ea5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8ea5-139">Requirements</span></span>



| <span data-ttu-id="c8ea5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8ea5-140">Requirement</span></span> | <span data-ttu-id="c8ea5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8ea5-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ea5-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8ea5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ea5-143">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8ea5-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8ea5-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8ea5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ea5-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8ea5-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8ea5-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c8ea5-146">End of client support</span></span><br/>    | <span data-ttu-id="c8ea5-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8ea5-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8ea5-148">Produit</span><span class="sxs-lookup"><span data-stu-id="c8ea5-148">Product</span></span><br/>                  | <span data-ttu-id="c8ea5-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8ea5-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8ea5-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8ea5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ea5-151"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8ea5-152">IID</span><span class="sxs-lookup"><span data-stu-id="c8ea5-152">IID</span></span><br/>                      | <span data-ttu-id="c8ea5-153">IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="c8ea5-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

