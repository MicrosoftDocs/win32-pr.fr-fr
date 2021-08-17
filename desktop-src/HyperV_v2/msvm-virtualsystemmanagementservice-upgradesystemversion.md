---
description: Met à niveau le système virtuel.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Méthode UpgradeSystemVersion de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64146c146bfd2c05d96e11d5193e246c76a6d1eb247d240b712cb46367a698c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148012"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode UpgradeSystemVersion de la \_ classe VirtualSystemManagementService MSVM

Met à niveau le système virtuel.

En cas d’application aux paramètres système d’une configuration de système virtuel « en cours »

## <a name="syntax"></a>Syntaxe


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui représente le système d’ordinateur virtuel à mettre à niveau.

</dd> <dt>

*UpgradeSettingData* \[ dans\]
</dt> <dd>

Données du paramètre de mise à niveau.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
</dt> <dt>

**État non valide** (5)
</dt> <dt>

**Paramètres incompatibles** (6)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

