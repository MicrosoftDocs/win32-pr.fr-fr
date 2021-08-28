---
title: IVMVirtualPC MaximumParallelPortsPerVM, propriété (VPCCOMInterfaces. h)
description: Récupère le nombre maximal de ports parallèles par ordinateur virtuel.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- MaximumParallelPortsPerVM propriété Virtual PC
- MaximumParallelPortsPerVM, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété MaximumParallelPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1449f3a32c606d6a326cb67d3169506408ee47dfc007d22970281c70d0a78b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056547"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a>IVMVirtualPC :: MaximumParallelPortsPerVM, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre maximal de ports parallèles par ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre maximal de ports parallèles par ordinateur virtuel.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                           | Signification                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre a la **valeur null**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

