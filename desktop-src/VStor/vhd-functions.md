---
description: 'En savoir plus sur : <span id=vhd.vhd_functions></span> fonctions de disque virtuel'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Fonctions de disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514439"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="478b1-103"><span id="vhd.vhd_functions"></span>Fonctions de disque virtuel</span><span class="sxs-lookup"><span data-stu-id="478b1-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="478b1-104">Les fonctions suivantes sont utilisées dans les disques virtuels :</span><span class="sxs-lookup"><span data-stu-id="478b1-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="478b1-105"><span id="in_this_section"></span>Dans cette section</span><span class="sxs-lookup"><span data-stu-id="478b1-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="478b1-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="478b1-106">Topic</span></span></th>
<th><span data-ttu-id="478b1-107">Description</span><span class="sxs-lookup"><span data-stu-id="478b1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="478b1-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-109">Applique un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="478b1-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-111">Attache un parent à un disque virtuel ouvert avec l’indicateur <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="478b1-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-113">Attache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur VHD approprié pour accomplir la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="478b1-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-115">Interrompt une opération de mise en miroir lancée précédemment et définit le miroir comme étant le disque virtuel actif.</span><span class="sxs-lookup"><span data-stu-id="478b1-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-117">Réduit la taille d’un fichier de magasin de stockage de disque dur virtuel (VHD).</span><span class="sxs-lookup"><span data-stu-id="478b1-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-119">Crée un fichier image de disque dur virtuel (VHD), soit à l’aide de paramètres par défaut, soit à l’aide d’un disque virtuel ou d’un disque physique existant.</span><span class="sxs-lookup"><span data-stu-id="478b1-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-121">Supprime un instantané d’un fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-123">Supprime les métadonnées d’un disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-125">Détache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur de disque virtuel approprié pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="478b1-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-127">Énumère les métadonnées associées à un disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-129">Augmente la taille d’un disque dur virtuel fixe ou extensible dynamiquement (VHD).</span><span class="sxs-lookup"><span data-stu-id="478b1-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-131">Retourne les relations entre les disques durs virtuels (VHD) ou le fichier image de CD ou DVD (ISO) ou les volumes contenus dans ces disques et leur disque ou volume parent.</span><span class="sxs-lookup"><span data-stu-id="478b1-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-133">Récupère des informations sur un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-135">Récupère les métadonnées spécifiées à partir du disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-137">Vérifie la progression d’une opération de disque dur virtuel (VHD) asynchrone.</span><span class="sxs-lookup"><span data-stu-id="478b1-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-139">Récupère le chemin d’accès à l’objet d’appareil physique qui contient un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO).</span><span class="sxs-lookup"><span data-stu-id="478b1-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-141">Fusionne un disque dur virtuel (VHD) enfant dans une chaîne de différenciation avec un ou plusieurs disques virtuels parents dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="478b1-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-143">Lance une opération de mise en miroir pour un disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-145">Modifie le contenu interne d’un fichier de disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="478b1-146">Peut être utilisé pour définir la feuille active ou pour corriger les entrées d’instantané.</span><span class="sxs-lookup"><span data-stu-id="478b1-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-148">Ouvre un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="478b1-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-150">Récupère des informations sur les modifications apportées aux zones spécifiées d’un disque dur virtuel (VHD) qui sont suivies par le suivi des modifications résilientes (RCT).</span><span class="sxs-lookup"><span data-stu-id="478b1-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-152">Émet une requête SCSI incorporée directement sur un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-154">Redimensionne un disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-156">Définit des informations sur un disque dur virtuel (VHD).</span><span class="sxs-lookup"><span data-stu-id="478b1-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478b1-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-158">Définit un élément de métadonnées pour un disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="478b1-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478b1-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="478b1-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="478b1-160">Crée un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="478b1-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
