---
description: Représente l’occurrence d’un événement qui est supprimé. Un événement supprimé est un événement qui n’est pas remis à un consommateur d’événements.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Classe __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523339"
---
# <a name="__eventdroppedevent-class"></a>\_\_EventDroppedEvent, classe

La classe système **\_ \_ EventDroppedEvent** représente l’occurrence d’un événement qui est supprimé. Un événement supprimé est un événement qui n’est pas remis à un consommateur d’événements.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventDroppedEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventDroppedEvent** possède les propriétés suivantes.

<dl> <dt>

**Event**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ événement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Événement qui est supprimé.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ EventConsumer**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) qui représente le consommateur permanent que vous identifiez pour recevoir un événement. Différents consommateurs permanents qui s’abonnent à un événement peuvent continuer à recevoir l’événement.

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par un fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir un événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure de génération d’un événement. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ EventDroppedEvent** est dérivée de [**\_ \_ SystemEvent**](--systemevent.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

