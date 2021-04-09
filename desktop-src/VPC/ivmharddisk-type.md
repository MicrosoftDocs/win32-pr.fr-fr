---
title: Propriété de type IVMHardDisk (VPCCOMInterfaces. h)
description: Type du disque dur virtuel.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propriété de type Virtual PC
- Propriété de type Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, type, propriété
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032818"
---
# <a name="ivmharddisktype-property"></a>IVMHardDisk :: type, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le type du disque dur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Valeur de la propriété

Type de l’image de disque dur actuelle.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                  |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                     |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le fichier image de disque dur actuel est introuvable.<br/>                           |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl>                         | Le type de l’image actuelle du disque dur n’est pas valide.<br/>                            |
| <dl> <dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt> </dl>                  | Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.<br/>   |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt> </dl>                      | Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                              |



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

 

