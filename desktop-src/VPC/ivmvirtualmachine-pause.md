---
title: IVMVirtualMachine pause, méthode (VPCCOMInterfaces. h)
description: Suspend la machine virtuelle.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Suspendre la méthode Virtual PC
- Suspendre la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, pause, méthode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843945"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine ::P méthode ause

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Suspend la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'opération a réussi.<br/>                                     |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>                                     | La machine virtuelle est déjà suspendue.<br/>                                         |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt> </dl> | L’appelant doit avoir des autorisations d’accès en exécution pour suspendre cette machine virtuelle.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                           | L’opération ne s’est pas terminée en temps opportun.<br/>                |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                     | L’ordinateur virtuel n’est pas en cours d’exécution.<br/>                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                          | La configuration est inconnue.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                          | Une erreur inattendue s’est produite.<br/>                                 |



 

## <a name="remarks"></a>Notes

La **suspension** n’enregistre pas l’état actuel de la machine virtuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

