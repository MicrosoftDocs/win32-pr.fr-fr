---
description: Crée un pool de ressources enfant.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Méthode CreatePool de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534616"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Méthode CreatePool de la \_ classe ResourcePoolConfigurationService MSVM

Crée un pool de ressources enfant. Le pool de ressources sera étendu au même système que ce service. Le pool résultant sera un pool enfant.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PoolSettings* \[ dans\]
</dt> <dd>

Une instance incorporée de la classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilisée pour spécifier les paramètres du pool qui ne sont pas liés à l’allocation.

</dd> <dt>

*ParentPools* \[ dans\]
</dt> <dd>

Tableau de références [**\_ ResourcePool MSVM**](msvm-resourcepool.md) qui représentent le ou les pools à partir desquels créer le pool.

</dd> <dt>

*AllocationSettings* \[ dans\]
</dt> <dd>

Tableau d’une ou de plusieurs instances incorporées de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui sont utilisées pour spécifier les paramètres liés à l’allocation du pool. Ce tableau doit contenir un élément pour chaque élément dans le tableau *ParentPools* ou exactement un élément. Si ce tableau contient un élément et que *ParentPools* contient plusieurs éléments, *AlllocationSettings* spécifie une allocation de capacité partagée qui peut être satisfaite par l’un des pools parents.

Cela permet de restreindre les ressources qui peuvent être allouées de l’enfant au pool à une limite inférieure à la capacité d’agrégation fournie par ses parents. Cette option n’est pas prise en charge par tous les types de ressources. Si un type de ressource ne prend pas en charge l’allocation de capacité partagée, cette méthode retourne 32770 (non pris en charge).

</dd> <dt>

*Pool* \[ à\]
</dt> <dd>

Référence au pool résultant.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Tâche terminée sans erreur** (0)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**Inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

**En cours d’utilisation** (32774)
</dt> <dt>

**État non valide** (32775)
</dt> <dt>

**Type de ressource incorrect pour le pool** (32776)
</dt> <dt>

**Non disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> <dt>

**Fournisseur réservé** (32779)
</dt> <dt>

**Ressources insuffisantes** (32780)
</dt> <dt>

**Objet introuvable** (32781.. 32787)
</dt> <dt>

L' **objet existe** (32788)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
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

[**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

