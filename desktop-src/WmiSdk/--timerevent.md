---
description: Signale un événement généré par WMI en réponse à une demande de consommateurs pour un événement de minuteur d’intervalle ou un événement de minuteur absolu.
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: Classe __TimerEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5615d5ec4beabed3eada6db1f78c3a5b7e0ea2a0e18ca074d0a95cd7173f7bcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109673"
---
# <a name="__timerevent-class"></a>\_\_TimerEvent, classe

La classe système **\_ \_ TimerEvent** indique un événement généré par WMI en réponse à la demande d’un consommateur pour un événement d’horloge d’intervalle ou un événement de minuterie absolu. Un événement de minuteur d’intervalle est un événement qui se produit à intervalles réguliers. Un événement de minuteur absolu est un événement qui se produit à un moment donné. Les événements de minuterie peuvent se produire dans n’importe quel espace de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ TimerEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ TimerEvent** possède les propriétés suivantes.

<dl> <dt>

**NumFirings**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de fois où l’événement s’est produit avant la remise d’une notification au consommateur.

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

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC). Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance de la sous-classe [**\_ \_ TimerInstruction**](--timerinstruction.md) qui a provoqué le déclenchement de cet événement par WMI. Les consommateurs spécifient une identification de minuteur dans la propriété **timerId** de la sous-classe **\_ \_ TimerInstruction** qu’ils créent pour s’inscrire.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ TimerEvent** est dérivée de [**\_ \_ Event**](--event.md).

Les consommateurs d’événements s’inscrivent pour un événement de minuteur absolu en créant une instance de la classe système [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) . Ils s’inscrivent pour un événement de minuteur d’intervalle en créant une instance de la classe système [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

Pendant un fonctionnement normal, la propriété **NumFirings** a la valeur 1. Lorsqu’il n’est pas possible d’atteindre le consommateur ou que l’intervalle de déclenchement est bien plus rapide que la capacité à remettre l’événement, **NumFirings** est défini sur un nombre supérieur à 1. Lorsque **NumFirings** est supérieur à 1, WMI fusionne automatiquement un grand nombre d’événements de minuterie dans le même événement. cette fusion est similaire à ce qui se produit avec les messages [**\_ du minuteur WM**](/windows/desktop/winmsg/wm-timer) dans Windows programmation.

## <a name="requirements"></a>Conditions requises



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

[Réception d’événements chronométrés ou répétitifs](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

