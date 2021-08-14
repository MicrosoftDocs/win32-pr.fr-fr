---
title: IVMVirtualMachine UndoAction, propriété (VPCCOMInterfaces. h)
description: Action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est arrêtée.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction, propriété Virtual PC
- UndoAction, propriété Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, UndoAction, propriété
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed32b0864e1a22b196001c5f75ba7e58711e7a9b6d6b2781a5f75ae0c3ced5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344544"
---
# <a name="ivmvirtualmachineundoaction-property"></a>IVMVirtualMachine :: UndoAction, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit l’action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est désactivée à l’aide de la méthode [**turnoff**](ivmvirtualmachine-turnoff.md) ou qu’elle est arrêtée à l’aide de la méthode [**Shutdown**](ivmguestos-shutdown.md) ou désactivée dans le système d’exploitation invité.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie l’action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est arrêtée depuis le système d’exploitation invité. Pour obtenir la liste des valeurs, consultez [**VMUndoAction**](vmundoaction.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | Ce paramètre n'est pas valide.<br/>       |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>     |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



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

 

