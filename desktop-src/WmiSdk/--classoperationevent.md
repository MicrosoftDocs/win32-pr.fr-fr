---
description: Est une classe de base pour tous les événements intrinsèques liés à une classe.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Classe __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 52ff5854d5510b22eaf264bcdbbfd39bbb02c7d2a2766eb3fbd8f336bd0b8074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860609"
---
# <a name="__classoperationevent-class"></a>\_\_ClassOperationEvent, classe

La classe système **\_ \_ ClassOperationEvent** est une classe de base pour tous les événements intrinsèques liés à une classe.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ClassOperationEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ClassOperationEvent** possède les propriétés suivantes.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**TargetClass**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Classe affectée par l’événement. Pour les événements de création, il s’agit de la classe nouvellement créée. Pour les événements de modification, il s’agit de la nouvelle version de la classe modifiée. Pour les événements de suppression, il s’agit de la classe supprimée.

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ ClassOperationEvent** est dérivée de [**\_ \_ Event**](--event.md).

Les instances de **\_ \_ ClassOperationEvent** ne sont pas créées ; seules les instances de ses sous-classes sont créées. Les classes suivantes dérivent de **\_ \_ ClassOperationEvent**:

[**\_\_ClassCreationEvent**](--classcreationevent.md)

[**\_\_ClassModificationEvent**](--classmodificationevent.md)

[**\_\_ClassDeletionEvent**](--classdeletionevent.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_Événement**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

