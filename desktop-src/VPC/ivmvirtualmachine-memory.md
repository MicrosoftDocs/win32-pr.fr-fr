---
title: Propriété mémoire IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantité de mémoire physique de l’ordinateur virtuel, en mégaoctets.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propriété mémoire Virtual PC
- Propriété mémoire Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété mémoire
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a828dde1804e546c97fe7cd2c161fc45366d416ba0e44900816c7bbee4b1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344663"
---
# <a name="ivmvirtualmachinememory-property"></a>IVMVirtualMachine :: Memory, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit la quantité de mémoire physique de l’ordinateur virtuel, en mégaoctets.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie la quantité de mémoire physique, en mégaoctets.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                         | Signification                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'opération a réussi.<br/>                  |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>              | Le paramètre a la **valeur null**.<br/>                     |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | Le paramètre n’est pas valide ou est hors limites.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>      | La configuration est inconnue.<br/>                  |
| <dl> <dt>Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables</dt> <dt>0xA0040300</dt> </dl> | La préférence est introuvable.<br/>                  |
| <dl> <dt>Ordinateur virtuel \_ E/r 0xA0040302 \_ \_ \_ active VM</dt> <dt></dt> </dl> | L’ordinateur virtuel est en cours d’exécution ou enregistré.<br/>       |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>      | Une erreur inattendue s’est produite.<br/>              |



## <a name="remarks"></a>Remarques

La quantité de mémoire physique d’un ordinateur virtuel doit être d’au moins 4 Mo. La limite supérieure de la mémoire dépend de la configuration de l’hôte, mais elle peut être d’au plus 3 712 Mo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

