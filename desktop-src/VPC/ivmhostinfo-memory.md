---
title: Propriété mémoire IVMHostInfo (VPCCOMInterfaces. h)
description: Récupère la quantité totale de mémoire physique de l’ordinateur hôte, en mégaoctets.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Propriété mémoire Virtual PC
- Propriété mémoire Virtual PC, interface IVMHostInfo
- IVMHostInfo interface Virtual PC, propriété mémoire
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22eeae9bcd7be7436d02f9aa116882acc4d8e0e8ee5d2703790b5e20cd4d744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753328"
---
# <a name="ivmhostinfomemory-property"></a>IVMHostInfo :: Memory, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la quantité totale de mémoire physique de l’ordinateur hôte, en mégaoctets.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a>Valeur de la propriété

Quantité totale de mémoire physique, en mégaoctets. Cette valeur est une **variante** de type VT \_ Decimal.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

