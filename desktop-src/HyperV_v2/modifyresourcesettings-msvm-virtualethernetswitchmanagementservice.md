---
description: Modifie les paramètres de ressource pour un commutateur virtuel.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Méthode ModifyResourceSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 05ed2a7e876cda87e0d8df60a03532edfcde6d4188dc74bf83edf06936f1127d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693949"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Méthode ModifyResourceSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM

Modifie les paramètres de ressource pour un commutateur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), qui contient les aspects modifiés des ressources virtuelles existantes. La propriété **InstanceID** de chaque instance identifie le paramètre de ressource virtuelle à modifier.

</dd> <dt>

*ResultingResourceSettings* \[ à\]
</dt> <dd>

Tableau de références aux instances d’objets dérivés de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) représentant les aspects virtuels des ressources virtuelles modifiées.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AddResourceSettings**](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveResourceSettings**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

