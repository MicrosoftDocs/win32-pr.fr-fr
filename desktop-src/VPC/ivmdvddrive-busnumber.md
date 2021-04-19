---
title: IVMDVDDrive BusNumber, propriété (VPCCOMInterfaces. h)
description: Récupère le numéro de bus auquel cet appareil est attaché.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- BusNumber propriété Virtual PC
- BusNumber, propriété Virtual PC, IVMDVDDrive, interface
- IVMDVDDrive interface Virtual PC, propriété BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509934"
---
# <a name="ivmdvddrivebusnumber-property"></a>IVMDVDDrive :: BusNumber, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le numéro de bus auquel cet appareil est attaché.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de bus. Par exemple, sur un bus IDE, cette valeur représente l’emplacement principal ou secondaire.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                       | Signification                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | L'opération a réussi.<br/>                                          |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>            | Le paramètre a la **valeur null**.<br/>                                             |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt> </dl> | L’emplacement du bus pour ce lecteur de DVD n’a pas été correctement initialisé.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>    | Une erreur inattendue s’est produite.<br/>                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

