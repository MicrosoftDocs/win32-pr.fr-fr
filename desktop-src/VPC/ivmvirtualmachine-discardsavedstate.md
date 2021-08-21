---
title: Méthode IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Ignore toutes les informations d’état enregistrées pour un ordinateur virtuel enregistré.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Méthode DiscardSavedState Virtual PC
- Méthode DiscardSavedState Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff30406328ae13004505440ae2fb8b18b2e1fdf8ac19dcbfbe77b063e54df688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471979"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine ::D méthode iscardSavedState

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ignore toutes les informations d’état enregistrées pour un ordinateur virtuel enregistré.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                           | Description                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                 | L'opération a réussi.<br/>                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>           | La configuration est inconnue.<br/>                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt> </dl>           | La machine virtuelle est en cours d’exécution.<br/>                             |
| <dl> <dt>**Ordinateur virtuel \_ E \_ VM \_ sans \_ \_ état enregistré**</dt> <dt>0xA00400501</dt> </dl> | L’ordinateur virtuel n’est pas en cours d’exécution, mais il n’a pas d’état enregistré.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>           | Une erreur inattendue s’est produite.<br/>                           |



 

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

 

