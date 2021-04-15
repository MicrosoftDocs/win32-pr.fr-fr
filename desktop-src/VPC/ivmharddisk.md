---
title: Interface IVMHardDisk (VPCCOMInterfaces. h)
description: Permet d’accéder à une image de disque dur. Elle est accessible par le biais de la propriété IVMHardDiskConnection de la méthode IVMVirtualPC ou GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Virtual PC de l’interface IVMHardDisk
- IVMHardDisk interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464190"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="b8462-106">Interface IVMHardDisk</span><span class="sxs-lookup"><span data-stu-id="b8462-106">IVMHardDisk interface</span></span>

<span data-ttu-id="b8462-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8462-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8462-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8462-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8462-109">Permet d’accéder à une image de disque dur.</span><span class="sxs-lookup"><span data-stu-id="b8462-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="b8462-110">Elle est accessible par le biais de la méthode [**IVMHardDiskConnection :: dur**](ivmharddiskconnection-harddisk.md) ou de la méthode [**IVMVirtualPC :: GetHardDisk**](ivmvirtualpc-getharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="b8462-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="b8462-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b8462-111">Members</span></span>

<span data-ttu-id="b8462-112">L’interface **IVMHardDisk** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b8462-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b8462-113">**IVMHardDisk** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8462-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="b8462-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8462-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8462-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8462-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8462-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8462-116">Methods</span></span>

<span data-ttu-id="b8462-117">L’interface **IVMHardDisk** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b8462-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="b8462-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8462-118">Method</span></span>                                 | <span data-ttu-id="b8462-119">Description</span><span class="sxs-lookup"><span data-stu-id="b8462-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8462-120">**Compact**</span><span class="sxs-lookup"><span data-stu-id="b8462-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="b8462-121">Compacte une image de disque dur virtuel de taille dynamique.</span><span class="sxs-lookup"><span data-stu-id="b8462-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="b8462-122">**Convertir**</span><span class="sxs-lookup"><span data-stu-id="b8462-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="b8462-123">Convertit n’importe quel disque dur virtuel en disque dur virtuel de taille dynamique ou en disque dur virtuel de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="b8462-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="b8462-124">**Fusion**</span><span class="sxs-lookup"><span data-stu-id="b8462-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="b8462-125">Fusionne un disque dur virtuel de différenciation avec son image de disque parent.</span><span class="sxs-lookup"><span data-stu-id="b8462-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="b8462-126">**MergeTo**</span><span class="sxs-lookup"><span data-stu-id="b8462-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="b8462-127">Fusionne un disque dur virtuel de différenciation avec tous ses parents (jusqu’à et y compris le disque dur virtuel parent racine) vers un nouveau fichier de disque dur.</span><span class="sxs-lookup"><span data-stu-id="b8462-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8462-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8462-128">Properties</span></span>

<span data-ttu-id="b8462-129">L’interface **IVMHardDisk** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8462-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="b8462-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="b8462-130">Property</span></span>                                                              | <span data-ttu-id="b8462-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b8462-131">Access type</span></span>           | <span data-ttu-id="b8462-132">Description</span><span class="sxs-lookup"><span data-stu-id="b8462-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8462-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b8462-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="b8462-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8462-134">Read-only</span></span><br/>  | <span data-ttu-id="b8462-135">Nom du chemin d’accès complet du fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="b8462-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="b8462-136">**HostFreeDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="b8462-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="b8462-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8462-137">Read-only</span></span><br/>  | <span data-ttu-id="b8462-138">Quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="b8462-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="b8462-139">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b8462-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="b8462-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b8462-140">Read/write</span></span><br/> | <span data-ttu-id="b8462-141">Parent du disque dur virtuel de différenciation.</span><span class="sxs-lookup"><span data-stu-id="b8462-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="b8462-142">**SizeInGuest**</span><span class="sxs-lookup"><span data-stu-id="b8462-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="b8462-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8462-143">Read-only</span></span><br/>  | <span data-ttu-id="b8462-144">Taille du disque dur virtuel dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="b8462-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="b8462-145">**SizeOnHost**</span><span class="sxs-lookup"><span data-stu-id="b8462-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="b8462-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8462-146">Read-only</span></span><br/>  | <span data-ttu-id="b8462-147">Taille du fichier de disque dur virtuel sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="b8462-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="b8462-148">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="b8462-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="b8462-149">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8462-149">Read-only</span></span><br/>  | <span data-ttu-id="b8462-150">Type du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="b8462-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="b8462-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8462-151">Requirements</span></span>



| <span data-ttu-id="b8462-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8462-152">Requirement</span></span> | <span data-ttu-id="b8462-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8462-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8462-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8462-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b8462-155">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8462-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8462-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8462-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b8462-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8462-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8462-158">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b8462-158">End of client support</span></span><br/>    | <span data-ttu-id="b8462-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8462-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8462-160">Produit</span><span class="sxs-lookup"><span data-stu-id="b8462-160">Product</span></span><br/>                  | <span data-ttu-id="b8462-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8462-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8462-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8462-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8462-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8462-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8462-164">IID</span><span class="sxs-lookup"><span data-stu-id="b8462-164">IID</span></span><br/>                      | <span data-ttu-id="b8462-165">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b8462-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

