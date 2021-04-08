---
title: IVMAccountant DiskBytesWritten, propriété (VPCCOMInterfaces. h)
description: Nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- DiskBytesWritten propriété Virtual PC
- DiskBytesWritten, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété DiskBytesWritten
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844274"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a>IVMAccountant ::D propriété iskBytesWritten

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre total d'octets lus. Ces données sont retournées sous la forme d’un **Variant** de type **VT \_ Decimal**.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>       |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>          |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                    | L’ordinateur virtuel n’est pas en cours d’exécution.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>   |



## <a name="remarks"></a>Notes

Notez que les statistiques d’e/s disque sont réinitialisées à zéro lorsqu’une machine virtuelle est mise sous tension, réinitialisée ou restaurée à partir de l’état enregistré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

