---
title: Énumération VMShutdownAction (VPCCOMInterfaces. h)
description: Indique comment arrêter un ordinateur virtuel lorsque l’ordinateur hôte s’arrête ou que le processus de vpc.exe se termine.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Virtual PC de l’énumération VMShutdownAction
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1f8b5bc21021e7771c14c0c3c6399e1d6342d7ebe3803759c8adb5c45024cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248409"
---
# <a name="vmshutdownaction-enumeration"></a>Énumération VMShutdownAction

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indique comment arrêter un ordinateur virtuel (VM) lorsque l’ordinateur hôte s’arrête ou que le processus de vpc.exe se termine.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ Enregistrer**
</dt> <dd>

Enregistrez l’état de la machine virtuelle.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ turnoff**
</dt> <dd>

Désactivez la machine virtuelle sans annuler les lecteurs.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**arrêt de vmShutdownAction \_**
</dt> <dd>

Arrêtez le système d’exploitation invité sur la machine virtuelle sans annuler les lecteurs si les composants d’intégration sont disponibles et enregistrera la machine virtuelle dans le cas contraire.

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

[Windows Énumérations de PC virtuels](virtual-pc-enumerations.md)
</dt> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

