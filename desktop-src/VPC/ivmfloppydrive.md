---
title: Interface IVMFloppyDrive (VPCCOMInterfaces. h)
description: Contrôle un lecteur de disquette au sein d’une machine virtuelle.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Virtual PC de l’interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942681"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="1b83d-105">Interface IVMFloppyDrive</span><span class="sxs-lookup"><span data-stu-id="1b83d-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="1b83d-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1b83d-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1b83d-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1b83d-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1b83d-108">Contrôle un lecteur de disquette au sein d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1b83d-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="1b83d-109">**IVMFloppyDrive** peut informer les clients des événements à l’aide de l’interface sortante [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="1b83d-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="1b83d-110">Vous pouvez récupérer un objet **IVMFloppyDrive** à partir de l’objet [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="1b83d-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="1b83d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1b83d-111">Members</span></span>

<span data-ttu-id="1b83d-112">L’interface **IVMFloppyDrive** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1b83d-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1b83d-113">**IVMFloppyDrive** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1b83d-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="1b83d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b83d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b83d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b83d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b83d-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b83d-116">Methods</span></span>

<span data-ttu-id="1b83d-117">L’interface **IVMFloppyDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1b83d-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="1b83d-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="1b83d-118">Method</span></span>                                                      | <span data-ttu-id="1b83d-119">Description</span><span class="sxs-lookup"><span data-stu-id="1b83d-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b83d-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="1b83d-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="1b83d-121">Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1b83d-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="1b83d-122">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="1b83d-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="1b83d-123">Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="1b83d-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="1b83d-124">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="1b83d-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="1b83d-125">Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="1b83d-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="1b83d-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="1b83d-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="1b83d-127">Libère une image de support de disquette sur l’ordinateur hôte à partir du lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="1b83d-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="1b83d-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b83d-128">Properties</span></span>

<span data-ttu-id="1b83d-129">L’interface **IVMFloppyDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b83d-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="1b83d-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="1b83d-130">Property</span></span>                                                             | <span data-ttu-id="1b83d-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1b83d-131">Access type</span></span>          | <span data-ttu-id="1b83d-132">Description</span><span class="sxs-lookup"><span data-stu-id="1b83d-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b83d-133">**Pièce jointe**</span><span class="sxs-lookup"><span data-stu-id="1b83d-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="1b83d-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b83d-134">Read-only</span></span><br/> | <span data-ttu-id="1b83d-135">Type de support attaché au lecteur de disquette au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1b83d-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="1b83d-136">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="1b83d-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="1b83d-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b83d-137">Read-only</span></span><br/> | <span data-ttu-id="1b83d-138">Index de base zéro du contrôleur auquel ce lecteur de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="1b83d-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="1b83d-139">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="1b83d-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="1b83d-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b83d-140">Read-only</span></span><br/> | <span data-ttu-id="1b83d-141">Lettre du lecteur hôte auquel le lecteur de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="1b83d-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="1b83d-142">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="1b83d-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="1b83d-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b83d-143">Read-only</span></span><br/> | <span data-ttu-id="1b83d-144">Chemin d’accès complet du fichier image auquel le lecteur de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="1b83d-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="1b83d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b83d-145">Requirements</span></span>



| <span data-ttu-id="1b83d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b83d-146">Requirement</span></span> | <span data-ttu-id="1b83d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b83d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b83d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b83d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1b83d-149">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b83d-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b83d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b83d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1b83d-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b83d-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1b83d-152">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1b83d-152">End of client support</span></span><br/>    | <span data-ttu-id="1b83d-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1b83d-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1b83d-154">Produit</span><span class="sxs-lookup"><span data-stu-id="1b83d-154">Product</span></span><br/>                  | <span data-ttu-id="1b83d-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1b83d-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1b83d-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b83d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b83d-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b83d-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1b83d-158">IID</span><span class="sxs-lookup"><span data-stu-id="1b83d-158">IID</span></span><br/>                      | <span data-ttu-id="1b83d-159">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="1b83d-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

