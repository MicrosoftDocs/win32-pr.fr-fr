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
ms.openlocfilehash: 5268f2cad452cad907f12031996e1d3092d9a91c0f52f8c045e1bfeaebc53f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654409"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a>IVMAccountant ::D propriété iskBytesWritten

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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



## <a name="remarks"></a>Remarques

Notez que les statistiques d’e/s disque sont réinitialisées à zéro lorsqu’une machine virtuelle est mise sous tension, réinitialisée ou restaurée à partir de l’état enregistré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

