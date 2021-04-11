---
title: IVMHardDisk HostFreeDiskSpace, propriété (VPCCOMInterfaces. h)
description: Récupère la quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace propriété Virtual PC
- HostFreeDiskSpace, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105811"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>IVMHardDisk :: HostFreeDiskSpace, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valeur de la propriété

Quantité d’espace disque restant disponible sur l’ordinateur hôte pour le fichier image de disque dur actuel. Cette valeur est une **variante** de type VT \_ Decimal.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                            | Signification                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | L'opération a réussi.<br/>                                |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                 | Le paramètre a la **valeur null**.<br/>                                   |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt> </dl> | Le chemin d’accès au fichier de disque dur virtuel actuel n’est pas valide.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                         | Une erreur inattendue s’est produite.<br/>                            |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

