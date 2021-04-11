---
description: Modifie les paramètres d’un pool enfant qui ne sont pas liés à l’allocation.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Méthode ModifyPoolSettings de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204023"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Méthode ModifyPoolSettings de la \_ classe ResourcePoolConfigurationService MSVM

Modifie les paramètres d’un pool enfant qui ne sont pas liés à l’allocation.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ChildPool* \[ dans\]
</dt> <dd>

Référence à une instance de la classe [**\_ ResourcePool CIM**](cim-resourcepool.md) qui représente le pool enfant à modifier.

</dd> <dt>

*PoolSettings* \[ dans\]
</dt> <dd>

Une instance incorporée de la classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilisée pour spécifier les nouveaux paramètres pour le pool.

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

 

