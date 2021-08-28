---
description: Signale quand un événement est abandonné suite à un dépassement de capacité de la file d’attente de remise.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6fd31df9f84883c8b677ea4fef0431ed762b4cec2155cb3d600893a40e3e1d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612629"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_EventQueueOverflowEvent, classe

La classe système **\_ \_ EventQueueOverflowEvent** indique quand un événement est abandonné suite à un dépassement de capacité de la file d’attente de remise.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventQueueOverflowEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventQueueOverflowEvent** possède les propriétés suivantes.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille actuelle de la file d’attente, en octets. La valeur par défaut de cette propriété est 10 Mo pour toutes les files d’attente combinées.

</dd> <dt>

**Event**
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Événement d’intérêt. Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ EventConsumer**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence au consommateur prévu. Cette propriété est héritée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC, Coordinated Universal Time). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarques

Seuls les utilisateurs disposant de privilèges d’administrateur peuvent recevoir cet événement. La classe **\_ \_ EventQueueOverflowEvent** est dérivée de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

Pour plus d’informations, consultez la propriété [**MaximumQueueSize**](--eventconsumer.md) dans la classe [**\_ \_ EventConsumer**](--eventconsumer.md) et la propriété [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) dans la classe **\_ WMISetting Win32** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

