---
description: 'En savoir plus sur : <span id=vhd.vhd_functions></span> fonctions de disque virtuel'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Fonctions de disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477215"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Fonctions de disque virtuel

Les fonctions suivantes sont utilisées dans les disques virtuels :

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Dans cette section


| Rubrique | Description | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p> | <p>Applique un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p> | <p>Attache un parent à un disque virtuel ouvert avec l’indicateur <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p> | <p>Attache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur VHD approprié pour accomplir la pièce jointe.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p> | <p>Interrompt une opération de mise en miroir lancée précédemment et définit le miroir comme étant le disque virtuel actif.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p> | <p>Réduit la taille d’un fichier de magasin de stockage de disque dur virtuel (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p> | <p>Crée un fichier image de disque dur virtuel (VHD), soit à l’aide de paramètres par défaut, soit à l’aide d’un disque virtuel ou d’un disque physique existant.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p> | <p>Supprime un instantané d’un fichier de définition de disque dur virtuel.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p> | <p>Supprime les métadonnées d’un disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p> | <p>Détache un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) en localisant un fournisseur de disque virtuel approprié pour effectuer l’opération.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p> | <p>Énumère les métadonnées associées à un disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p> | <p>Augmente la taille d’un disque dur virtuel fixe ou extensible dynamiquement (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p> | <p>Retourne les relations entre les disques durs virtuels (VHD) ou le fichier image de CD ou DVD (ISO) ou les volumes contenus dans ces disques et leur disque ou volume parent.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p> | <p>Récupère des informations sur un disque dur virtuel.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p> | <p>Récupère les métadonnées spécifiées à partir du disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p> | <p>Vérifie la progression d’une opération de disque dur virtuel (VHD) asynchrone.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p> | <p>Récupère le chemin d’accès à l’objet d’appareil physique qui contient un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p> | <p>Fusionne un disque dur virtuel (VHD) enfant dans une chaîne de différenciation avec un ou plusieurs disques virtuels parents dans la chaîne.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p> | <p>Lance une opération de mise en miroir pour un disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p> | <p>Modifie le contenu interne d’un fichier de disque virtuel. Peut être utilisé pour définir la feuille active ou pour corriger les entrées d’instantané.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p> | <p>Ouvre un disque dur virtuel (VHD) ou un fichier image de CD ou DVD (ISO) à utiliser.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p> | <p>Récupère des informations sur les modifications apportées aux zones spécifiées d’un disque dur virtuel (VHD) qui sont suivies par le suivi des modifications résilientes (RCT).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p> | <p>Émet une requête SCSI incorporée directement sur un disque dur virtuel.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p> | <p>Redimensionne un disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p> | <p>Définit des informations sur un disque dur virtuel (VHD).</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p> | <p>Définit un élément de métadonnées pour un disque virtuel.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p> | <p>Crée un instantané du disque virtuel actuel pour les fichiers de définition de VHD.</p> | 


 

 

 
