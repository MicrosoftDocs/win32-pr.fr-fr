---
description: Démarrer un travail pour modifier un pool parent à l’aide des paramètres d’allocation spécifiés.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Méthode ChangeParentResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7030cb4ed9333ad5c56722954a24a1ee7bff351a15873423dbfe6e8dca1830d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980899"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Méthode ChangeParentResourcePool de la \_ classe CIM ResourcePoolConfigurationService

Démarrer un travail pour modifier un pool parent à l’aide des paramètres d’allocation spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ChildPool* \[ dans\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) qui référence le pool enfant.

</dd> <dt>

*ParentPool* \[ dans\]
</dt> <dd>

Tableau [**\_ ResourcePool CIM**](cim-resourcepool.md) qui référence le ou les pools parents.

</dd> <dt>

*Paramètres* \[ dans\]
</dt> <dd>

Chaîne facultative contenant la représentation d’une instance [**CIM \_ SettingData**](cim-settingdata.md) utilisée pour spécifier les paramètres du pool parent.

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

 

 




