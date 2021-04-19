---
description: Signale un événement de suppression d’espace de noms, qui est un type d’événement intrinsèque qui est généré lorsqu’un sous-espace de noms est supprimé de l’espace de noms actuel.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Classe __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534733"
---
# <a name="__namespacedeletionevent-class"></a>\_\_NamespaceDeletionEvent, classe

La classe système **\_ \_ NamespaceDeletionEvent** signale un événement de suppression d’espace de noms, qui est un type d' [événement intrinsèque](determining-the-type-of-event-to-receive.md) qui est généré lorsqu’un sous-espace de noms est supprimé de l’espace de noms actuel.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ NamespaceDeletionEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ NamespaceDeletionEvent** possède les propriétés suivantes.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ espace de noms**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Copie de l’instance d' [**\_ \_ espace de noms**](--namespace.md) qui est supprimée. La propriété **Name** de l’instance d' **\_ \_ espace de noms** identifie l’espace de noms qui est supprimé. Cette propriété est héritée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

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

La classe **\_ \_ NamespaceDeletionEvent** est dérivée de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

