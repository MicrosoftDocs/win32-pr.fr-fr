---
title: Propriété MMX IVMHostInfo (VPCCOMInterfaces. h)
description: Détermine si le processeur prend en charge le jeu d’instructions MMX. | Propriété MMX IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- MMX, propriété Virtual PC
- MMX, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4498289130a59e7c651b9dfffe9d4d228f9d9187e9d958ce1d203291654d7c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998899"
---
# <a name="ivmhostinfommx-property"></a>IVMHostInfo :: MMX, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Détermine si le processeur prend en charge le jeu d’instructions MMX.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a>Valeur de la propriété

**True** si les instructions MMX sont prises en charge ; sinon, **false** .

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

 

