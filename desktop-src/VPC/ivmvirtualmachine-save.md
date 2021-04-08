---
title: Méthode Save IVMVirtualMachine (VPCCOMInterfaces. h)
description: Enregistre l’état de l’ordinateur virtuel.
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Enregistrer la méthode Virtual PC
- Enregistrer la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742884"
---
# <a name="ivmvirtualmachinesave-method"></a>IVMVirtualMachine :: Save, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Enregistre l’état de l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*saveTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence d’enregistrement de l’état de la machine virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'opération a réussi.<br/>                                                 |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>                                     | Impossible d’enregistrer la machine virtuelle, car les disques d’annulations ont été marqués pour suppression.<br/>    |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                  | Le paramètre a la **valeur null**.<br/>                                                    |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt> </dl> | L’appelant doit disposer des autorisations d’accès en exécution pour enregistrer l’état de cette machine virtuelle.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                     | La machine virtuelle n’est pas en cours d’exécution.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                          | Une erreur inattendue s’est produite.<br/>                                             |



 

## <a name="remarks"></a>Notes

La machine virtuelle est désactivée lorsque la tâche d' **enregistrement** atteint son achèvement. La propriété [**IVMVirtualMachine :: State**](ivmvirtualmachine-state.md) contiendra les **vmVMState d' \_ enregistrement** pendant l’enregistrement, puis les **vmVMState \_ enregistrées** lorsque l’enregistrement est terminé et que la machine virtuelle est désactivée.

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

 

