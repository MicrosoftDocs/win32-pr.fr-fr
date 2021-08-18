---
description: La méthode ModifyResourceSettings de la classe Msvm_VirtualSystemManagementService-modifie les paramètres de ressource virtuelle.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Méthode ModifyResourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ec7a2592bf6919616e424b7be22c6d5228a86ada16624d8732afd08d0f0be1dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693919"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode ModifyResourceSettings de la \_ classe VirtualSystemManagementService MSVM

Modifie les paramètres de ressource virtuelle. En cas d’application à des parties d’une configuration d’ordinateur virtuel active, en tant qu’effet secondaire, les ressources de la machine virtuelle active peuvent être modifiées.

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

[**ModifyVirtualSystemResources (v1)**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

