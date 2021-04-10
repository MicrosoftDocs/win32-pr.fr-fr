---
title: Propriété parente IVMHardDisk (VPCCOMInterfaces. h)
description: Parent du disque dur virtuel de différenciation.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propriété Parent Virtual PC
- Propriété Parent Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, propriété parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941635"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk ::P propriété rente

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit le parent du disque dur virtuel de différenciation.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit l’objet [**IVMHardDisk**](ivmharddisk.md) associé à l’image de disque dur parent.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                                               | Ce n’est pas un disque dur de différenciation, donc il n’a pas de parent.<br/>                                                                                                                                                                                                                 |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le système n’a pas pu trouver le fichier de disque dur virtuel parent.<br/>                                                                                                                                                                                                               |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt> </dl> | Le système n’a pas pu trouver le chemin d’accès au fichier de disque dur virtuel parent.<br/>                                                                                                                                                                                                   |
| <dl> <dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt> </dl>                  | Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.<br/>                                                                                                                                                                                               |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt> </dl>                      | Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.<br/>                                                                                                                                                                                             |
| <dl> <dt>Ordinateur virtuel \_ \_Incompatibilité \_ d' \_ ID \_ enfant parent E</dt> <dt>0xA0040685</dt> </dl>            | L’image de disque dur virtuel située dans le paramètre *parent* n’a pas le même ID que l’image de disque enfant. Assurez-vous que l’image de disque dur virtuel parent située dans le paramètre *parent* est la même que celle utilisée pour créer l’image de disque dur virtuel de différenciation.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Notes

Cette propriété est valide uniquement avec les images de disque dur de différenciation.

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

 

