---
description: Démarre un travail pour créer un ResourcePool racine. Le ResourcePool sera étendu au même système que ce service.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Méthode CreateResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 723ff669a44a7459f52a389e1ad61d236d00489a95e1bbf1038ce9c6eb21caab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980889"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Méthode CreateResourcePool de la \_ classe CIM ResourcePoolConfigurationService

Démarre un travail pour créer un ResourcePool racine. Le ResourcePool sera étendu au même système que ce service.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ElementName* \[ dans\]
</dt> <dd>

Nom approprié de l’utilisateur final pour le pool en cours de création. Si la **valeur est null**, un nom par défaut fourni par le système peut être utilisé. La valeur sera stockée dans la propriété **ElementName** pour le pool créé.

</dd> <dt>

*HostResources* \[ dans\]
</dt> <dd>

Tableau de zéro ou plusieurs [**périphériques \_ LogicalDevice CIM**](cim-logicaldevice.md) utilisés pour créer le pool ou pour modifier les étendues sources. Tous les éléments du tableau doivent être du même type.

</dd> <dt>

*ResourceType* \[ dans\]
</dt> <dd>

Le type de ressources que le pool créé doit gérer. Si *HostResources* contient des éléments, cette propriété doit avoir le même type.

</dd> <dt>

*Pool* \[ à\]
</dt> <dd>

En cas de réussite, retourne une référence au [**\_ ResourcePool CIM**](cim-resourcepool.md)résultant. Lorsqu’un travail est retourné, il peut s’agir de la **valeur null**, auquel cas le client doit utiliser le travail pour trouver le ResourcePool résultant une fois le travail terminé.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence à un [**\_ ConcreteJob CIM**](cim-concretejob.md) qui représente le travail (peut être null si le travail est terminé).

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

 

 




