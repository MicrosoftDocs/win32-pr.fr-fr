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
# <a name="ivmharddisk-interface"></a>Interface IVMHardDisk

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Permet d’accéder à une image de disque dur. Elle est accessible par le biais de la méthode [**IVMHardDiskConnection :: dur**](ivmharddiskconnection-harddisk.md) ou de la méthode [**IVMVirtualPC :: GetHardDisk**](ivmvirtualpc-getharddisk.md) .

## <a name="members"></a>Membres

L’interface **IVMHardDisk** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDisk** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMHardDisk** possède ces méthodes.



| Méthode                                 | Description                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compact**](ivmharddisk-compact.md) | Compacte une image de disque dur virtuel de taille dynamique.<br/>                                                                                        |
| [**Convertir**](ivmharddisk-convert.md) | Convertit n’importe quel disque dur virtuel en disque dur virtuel de taille dynamique ou en disque dur virtuel de taille fixe.<br/>                            |
| [**Fusion**](ivmharddisk-merge.md)     | Fusionne un disque dur virtuel de différenciation avec son image de disque parent.<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | Fusionne un disque dur virtuel de différenciation avec tous ses parents (jusqu’à et y compris le disque dur virtuel parent racine) vers un nouveau fichier de disque dur.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMHardDisk** possède les propriétés suivantes.



| Propriété                                                              | Type d’accès           | Description                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Fichier**](ivmharddisk-file.md)<br/>                           | Lecture seule<br/>  | Nom du chemin d’accès complet du fichier de disque dur virtuel.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Lecture seule<br/>  | Quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.<br/> |
| [**Parent**](ivmharddisk-parent.md)<br/>                       | Lecture/écriture<br/> | Parent du disque dur virtuel de différenciation.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Lecture seule<br/>  | Taille du disque dur virtuel dans le système d’exploitation invité.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Lecture seule<br/>  | Taille du fichier de disque dur virtuel sur l’ordinateur hôte.<br/>                        |
| [**Entrer**](ivmharddisk-type.md)<br/>                           | Lecture seule<br/>  | Type du disque dur virtuel.<br/>                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



 

