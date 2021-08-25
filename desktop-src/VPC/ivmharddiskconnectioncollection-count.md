---
title: Propriété Count IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de connexions de disque dur dans cette collection.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMHardDiskConnectionCollection, interface
- IVMHardDiskConnectionCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccb00cf2388db8a971f5da2f726030b3f793ac878f4a59df2646195eb41ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974322"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a>IVMHardDiskConnectionCollection :: Count, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre de connexions de disque dur dans cette collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de connexions de disque dur.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>     |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                               |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                      |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

