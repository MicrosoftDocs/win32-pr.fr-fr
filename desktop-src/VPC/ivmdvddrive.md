---
title: Interface IVMDVDDrive (VPCCOMInterfaces. h)
description: Contrôle un lecteur de CD-ROM ou de DVD-ROM au sein d’un ordinateur virtuel. IVMDVDDrive peut informer les clients des événements à l’aide de l’interface sortante IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Virtual PC de l’interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032996"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="de8a4-106">Interface IVMDVDDrive</span><span class="sxs-lookup"><span data-stu-id="de8a4-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="de8a4-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de8a4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="de8a4-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="de8a4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="de8a4-109">Contrôle un lecteur de CD-ROM ou de DVD-ROM au sein d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de8a4-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="de8a4-110">**IVMDVDDrive** peut informer les clients des événements à l’aide de l’interface sortante [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="de8a4-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="de8a4-111">Vous pouvez ajouter un nouveau lecteur de CD-ROM ou de DVD-ROM à une machine virtuelle à l’aide de la méthode [**IVMVirtualMachine :: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="de8a4-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="de8a4-112">Vous pouvez supprimer un lecteur de CD-ROM ou de DVD-ROM existant d’une machine virtuelle à l’aide de la méthode [**IVMVirtualMachine :: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="de8a4-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="de8a4-113">Vous pouvez récupérer un objet **IVMDVDDrive** à partir de l’objet [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) retourné à partir de la propriété [**IVMVirtualMachine ::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="de8a4-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="de8a4-114">Membres</span><span class="sxs-lookup"><span data-stu-id="de8a4-114">Members</span></span>

<span data-ttu-id="de8a4-115">L’interface **IVMDVDDrive** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="de8a4-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="de8a4-116">**IVMDVDDrive** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de8a4-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="de8a4-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de8a4-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="de8a4-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de8a4-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="de8a4-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de8a4-119">Methods</span></span>

<span data-ttu-id="de8a4-120">L’interface **IVMDVDDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="de8a4-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="de8a4-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="de8a4-121">Method</span></span>                                                   | <span data-ttu-id="de8a4-122">Description</span><span class="sxs-lookup"><span data-stu-id="de8a4-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="de8a4-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="de8a4-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="de8a4-124">Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de8a4-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="de8a4-125">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="de8a4-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="de8a4-126">Attache une image ISO au lecteur de DVD de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de8a4-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="de8a4-127">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="de8a4-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="de8a4-128">Libère un lecteur hôte capturé à partir du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="de8a4-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="de8a4-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="de8a4-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="de8a4-130">Libère une image ISO capturée à partir du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="de8a4-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="de8a4-131">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="de8a4-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="de8a4-132">Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="de8a4-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="de8a4-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de8a4-133">Properties</span></span>

<span data-ttu-id="de8a4-134">L’interface **IVMDVDDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="de8a4-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="de8a4-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="de8a4-135">Property</span></span>                                                          | <span data-ttu-id="de8a4-136">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="de8a4-136">Access type</span></span>          | <span data-ttu-id="de8a4-137">Description</span><span class="sxs-lookup"><span data-stu-id="de8a4-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="de8a4-138">**Pièce jointe**</span><span class="sxs-lookup"><span data-stu-id="de8a4-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="de8a4-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de8a4-139">Read-only</span></span><br/> | <span data-ttu-id="de8a4-140">Type de support attaché au lecteur de DVD au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="de8a4-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="de8a4-141">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="de8a4-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="de8a4-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de8a4-142">Read-only</span></span><br/> | <span data-ttu-id="de8a4-143">Numéro de bus auquel cet appareil est attaché.</span><span class="sxs-lookup"><span data-stu-id="de8a4-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="de8a4-144">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="de8a4-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="de8a4-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de8a4-145">Read-only</span></span><br/> | <span data-ttu-id="de8a4-146">Numéro de l’appareil auquel ce lecteur est attaché.</span><span class="sxs-lookup"><span data-stu-id="de8a4-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="de8a4-147">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="de8a4-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="de8a4-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de8a4-148">Read-only</span></span><br/> | <span data-ttu-id="de8a4-149">Lettre du lecteur hôte défini pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="de8a4-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="de8a4-150">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="de8a4-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="de8a4-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de8a4-151">Read-only</span></span><br/> | <span data-ttu-id="de8a4-152">Chemin d’accès complet du jeu de fichiers image pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="de8a4-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="de8a4-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de8a4-153">Requirements</span></span>



| <span data-ttu-id="de8a4-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de8a4-154">Requirement</span></span> | <span data-ttu-id="de8a4-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="de8a4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8a4-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de8a4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="de8a4-157">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de8a4-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de8a4-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de8a4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="de8a4-159">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="de8a4-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="de8a4-160">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="de8a4-160">End of client support</span></span><br/>    | <span data-ttu-id="de8a4-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de8a4-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="de8a4-162">Produit</span><span class="sxs-lookup"><span data-stu-id="de8a4-162">Product</span></span><br/>                  | <span data-ttu-id="de8a4-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de8a4-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="de8a4-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="de8a4-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="de8a4-165"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="de8a4-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="de8a4-166">IID</span><span class="sxs-lookup"><span data-stu-id="de8a4-166">IID</span></span><br/>                      | <span data-ttu-id="de8a4-167">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="de8a4-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

