---
title: IVMHostInfo DVDDrives, propriété (VPCCOMInterfaces. h)
description: Récupère les lettres de lecteur associées aux périphériques CD et DVD hôte.
ms.assetid: 17f01d00-2c02-48f0-bfe9-0326a40fdf55
keywords:
- DVDDrives propriété Virtual PC
- DVDDrives, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété DVDDrives
topic_type:
- apiref
api_name:
- IVMHostInfo.DVDDrives
- IVMHostInfo.get_DVDDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb9380773934b63ae637d32ec5acfef5112f2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384632"
---
# <a name="ivmhostinfodvddrives-property"></a>IVMHostInfo ::D propriété VDDrives

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère les lettres de lecteur associées aux périphériques CD et DVD hôte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DVDDrives(
  [out, retval] VARIANT *DVDDrives
);
```



## <a name="property-value"></a>Valeur de la propriété

Tableau de lettres de lecteur.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

