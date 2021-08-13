---
description: Démarrer un travail pour créer un sous-pool à partir d’un pool parent à l’aide des paramètres d’allocation spécifiés.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Méthode CreateChildResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48a43baeefcbc56707fa6327930d9c18eaa57a2442b81fbc5f5cff17633b2148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648151"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Méthode CreateChildResourcePool de la \_ classe CIM ResourcePoolConfigurationService

Démarrer un travail pour créer un sous-pool à partir d’un pool parent à l’aide des paramètres d’allocation spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ElementName* \[ dans\]
</dt> <dd>

Nom approprié de l’utilisateur final pour le pool en cours de création. Si la **valeur est null**, un nom par défaut fourni par le système peut être utilisé. La valeur sera stockée dans la propriété **ElementName** de l’élément créé.

</dd> <dt>

*Paramètres* \[ dans\]
</dt> <dd>

Chaîne contenant une représentation d’une instance de [**\_ SettingData CIM**](cim-settingdata.md) utilisée pour spécifier les paramètres du pool enfant.

</dd> <dt>

*ParentPool* \[ dans\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) à partir duquel créer le nouveau pool.

</dd> <dt>

*Pool* \[ à\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) qui fait référence au pool résultant.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence au travail (peut avoir la valeur null si le travail est terminé).

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

**Ressources insuffisantes** (8)
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

 

 




