---
title: Méthode IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Fusionne les disques d’annulations virtuelles.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Méthode MergeUndoDisks Virtual PC
- Méthode MergeUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d30558ddb8acdd75d72955048beb34f0141206b53f3f5873e42627fb155f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998679"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>IVMVirtualMachine :: MergeUndoDisks, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fusionne les disques d’annulations virtuelles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*undoMergeTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la création de l’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                            |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                                                                   |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* ou l’un des disques parents n’est pas valide.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier parent.<br/>                                                                 |
| <dl> <dt>**E \_ HANDLE**</dt> <dt>0x80070006</dt> </dl>                                     | Un des disques parents est en cours d’utilisation.<br/>                                                                                           |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                            | La configuration est inconnue.<br/>                                                                                                |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt> </dl>                            | La machine virtuelle est en cours d’exécution.<br/>                                                                                              |
| <dl> <dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt> </dl>                       | Le parent des disques d’annulations virtuelles est marqué en lecture seule.<br/>                                                                     |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                            |



 

## <a name="remarks"></a>Remarques

**MergeUndoDisks** ne peut pas être appelé tant que l’ordinateur virtuel est toujours en cours d’exécution. Utilisez [**IVMVirtualMachine :: Save**](ivmvirtualmachine-save.md) pour enregistrer l’état de l’ordinateur virtuel avant d’appeler **MergeUndoDisks** ou [**IVMVirtualMachine :: turnoff**](ivmvirtualmachine-turnoff.md) pour désactiver l’ordinateur virtuel sans enregistrer préalablement son état actuel.

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

 

