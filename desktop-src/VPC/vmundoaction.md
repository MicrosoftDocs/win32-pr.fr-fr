---
title: Énumération VMUndoAction (VPCCOMInterfaces. h)
description: Spécifie ce qui se passe pour annuler les lecteurs lorsqu’une machine virtuelle est arrêtée ou désactivée.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Virtual PC de l’énumération VMUndoAction
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f62c4ab00b30300b2951a5a6b1c300bf34b1b3797f036f28a66e82dc2cad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998329"
---
# <a name="vmundoaction-enumeration"></a>Énumération VMUndoAction

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie ce qui se passe pour annuler les lecteurs lorsqu’une machine virtuelle est arrêtée ou désactivée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction \_ Ignorer**
</dt> <dd>

Ignorer les lecteurs d’annulations ; les lecteurs parents restent inchangés.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ conserver**
</dt> <dd>

Conserver les disques d’annulations ; les lecteurs parents restent inchangés, mais les modifications sont conservées lors du prochain démarrage de la machine virtuelle.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**\_validation vmUndoAction**
</dt> <dd>

Valider les modifications apportées aux lecteurs parents.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine :: UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

