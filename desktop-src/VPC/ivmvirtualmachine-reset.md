---
title: Méthode de réinitialisation IVMVirtualMachine (VPCCOMInterfaces. h)
description: Réinitialise l’ordinateur virtuel.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Réinitialiser la méthode Virtual PC
- Réinitialiser la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466394"
---
# <a name="ivmvirtualmachinereset-method"></a>IVMVirtualMachine :: Reset, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Réinitialise l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de réinitialisation de la machine virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'opération a réussi.<br/>                                     |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                  | Le paramètre a la **valeur null**.<br/>                                        |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt> </dl> | L’appelant doit disposer des autorisations d’accès en exécution pour réinitialiser cet ordinateur virtuel.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                     | La machine virtuelle n’est pas en cours d’exécution.<br/>                                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                          | La configuration est inconnue.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                          | Une erreur inattendue s’est produite.<br/>                                 |



 

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

 

