---
title: Propriété Count IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de lecteurs de CD et de DVD dans ce regroupement.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMDVDDriveCollection, interface
- IVMDVDDriveCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510332"
---
# <a name="ivmdvddrivecollectioncount-property"></a>IVMDVDDriveCollection :: Count, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre de lecteurs de CD et de DVD dans ce regroupement.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de lecteurs de CD et DVD.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt> </dl>            | Une erreur inattendue s’est produite.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>     |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

