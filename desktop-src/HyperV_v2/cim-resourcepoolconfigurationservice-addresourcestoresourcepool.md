---
description: Démarre un travail pour ajouter des ressources à un pool de ressources.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Méthode AddResourcesToResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544692"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Méthode AddResourcesToResourcePool de la \_ classe CIM ResourcePoolConfigurationService

Démarre un travail pour ajouter des ressources à un pool de ressources.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HostResources* \[ dans\]
</dt> <dd>

Tableau d’instances [**CIM \_ LogicalDevice**](cim-logicaldevice.md) à ajouter au pool.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) qui représente le pool auquel ajouter les ressources.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

[**\_ ConcreteJob CIM**](cim-concretejob.md) qui référence le travail (peut être **null** si le travail est terminé).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

<dl> <dt>

**Tâche terminée sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Inconnu** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Échec** (4)
</dt> <dt>

**Paramètre non valide** (5)
</dt> <dt>

**En cours d’utilisation** (6)
</dt> <dt>

**ResourceType incorrect pour le pool** (7)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Taille non prise en charge** (4097)
</dt> <dt>

**Méthode réservée** (4098.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




