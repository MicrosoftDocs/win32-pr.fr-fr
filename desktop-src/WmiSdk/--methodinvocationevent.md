---
description: La \_ \_ classe système MethodInvocationEvent est définie, mais n’est pas implémentée.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Classe __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203974"
---
# <a name="__methodinvocationevent-class"></a>\_\_MethodInvocationEvent, classe

La classe système **\_ \_ MethodInvocationEvent** est définie, mais n’est pas implémentée.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ MethodInvocationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ MethodInvocationEvent** possède les propriétés suivantes.

<dl> <dt>

**Méthode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Méthode appelée pour déclencher l’événement.

</dd> <dt>

**Paramètres**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ paramètres**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance qui représente les paramètres d’entrée et de sortie de l’appel de méthode.

</dd> <dt>

**Préappel**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’événement est déclenché avant l’appel de la méthode.

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md). Pour plus d’informations, consultez [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance sur laquelle la méthode est appelée. Cette propriété est héritée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle un événement est généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ MethodInvocationEvent** est dérivée de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

