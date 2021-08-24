---
description: Injecte une interruption non masquable dans la machine virtuelle.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Msvm_ComputerSystem :: InjectNonMaskableInterrupt, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9019492299d03b31001b60934e00dc40c41b4328e4809fe8e864ef378c30a89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694439"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a>MSVM \_ ComputerSystem :: InjectNonMaskableInterrupt, méthode

Injecte une interruption non masquable dans la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) pour suivre l’état de l’injection d’interruptions. Cette référence peut être **null** si la tâche est terminée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Accès refusé** (32769)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

