---
description: Détermine si le système virtuel spécifié peut être migré.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Méthode CheckVirtualSystemIsMigratable de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862078"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Méthode CheckVirtualSystemIsMigratable de la \_ classe VirtualSystemMigrationService MSVM

Détermine si le système virtuel spécifié peut être migré.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance de la classe [**CIM \_ CIM**](cim-computersystem.md) qui représente l’ordinateur virtuel pour tester la capacité de migration de.

</dd> <dt>

*DestinationHost* \[ dans\]
</dt> <dd>

Nom du système hôte pour la migration. Le format de ce nom est spécifié par la propriété **DestinationHostFormatsSupported** de la [**classe \_ VirtualSystemMigrationCapabilities MSVM**](msvm-virtualsystemmigrationcapabilities.md) associée à cette classe.

</dd> <dt>

*MigrationSettingData* \[ dans\]
</dt> <dd>

Une instance incorporée de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) qui représente les paramètres de l’opération de migration.

</dd> <dt>

*NewSystemSettingData* \[ dans\]
</dt> <dd>

Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente les nouvelles propriétés applicables au système virtuel après sa migration.

</dd> <dt>

*NewResourceSettingData* \[ dans\]
</dt> <dd>

Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui représente les nouvelles propriétés applicables aux ressources virtuelles du système virtuel après qu’il a été migré.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

