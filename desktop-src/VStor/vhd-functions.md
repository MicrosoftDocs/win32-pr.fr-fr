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
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Fonctions de disque virtuel

Les fonctions suivantes sont utilisées dans les disques virtuels :

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Dans cette section

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p></td>
<td><p>Applique un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p></td>
<td><p>Attache un parent à un disque virtuel ouvert avec l’indicateur <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p></td>
<td><p>Attache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur VHD approprié pour accomplir la pièce jointe.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p></td>
<td><p>Interrompt une opération de mise en miroir lancée précédemment et définit le miroir comme étant le disque virtuel actif.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p></td>
<td><p>Réduit la taille d’un fichier de magasin de stockage de disque dur virtuel (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p></td>
<td><p>Crée un fichier image de disque dur virtuel (VHD), soit à l’aide de paramètres par défaut, soit à l’aide d’un disque virtuel ou d’un disque physique existant.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p></td>
<td><p>Supprime un instantané d’un fichier de définition de disque dur virtuel.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p></td>
<td><p>Supprime les métadonnées d’un disque virtuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p></td>
<td><p>Détache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur de disque virtuel approprié pour effectuer l’opération.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p></td>
<td><p>Énumère les métadonnées associées à un disque virtuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p></td>
<td><p>Augmente la taille d’un disque dur virtuel fixe ou extensible dynamiquement (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p></td>
<td><p>Retourne les relations entre les disques durs virtuels (VHD) ou le fichier image de CD ou DVD (ISO) ou les volumes contenus dans ces disques et leur disque ou volume parent.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p></td>
<td><p>Récupère des informations sur un disque dur virtuel.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p></td>
<td><p>Récupère les métadonnées spécifiées à partir du disque virtuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p></td>
<td><p>Vérifie la progression d’une opération de disque dur virtuel (VHD) asynchrone.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p></td>
<td><p>Récupère le chemin d’accès à l’objet d’appareil physique qui contient un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p></td>
<td><p>Fusionne un disque dur virtuel (VHD) enfant dans une chaîne de différenciation avec un ou plusieurs disques virtuels parents dans la chaîne.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p></td>
<td><p>Lance une opération de mise en miroir pour un disque virtuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p></td>
<td><p>Modifie le contenu interne d’un fichier de disque virtuel. Peut être utilisé pour définir la feuille active ou pour corriger les entrées d’instantané.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p></td>
<td><p>Ouvre un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) à utiliser.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p></td>
<td><p>Récupère des informations sur les modifications apportées aux zones spécifiées d’un disque dur virtuel (VHD) qui sont suivies par le suivi des modifications résilientes (RCT).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p></td>
<td><p>Émet une requête SCSI incorporée directement sur un disque dur virtuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p></td>
<td><p>Redimensionne un disque virtuel.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p></td>
<td><p>Définit des informations sur un disque dur virtuel (VHD).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p></td>
<td><p>Définit un élément de métadonnées pour un disque virtuel.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p></td>
<td><p>Crée un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</p></td>
</tr>
</tbody>
</table>

 

 

 
