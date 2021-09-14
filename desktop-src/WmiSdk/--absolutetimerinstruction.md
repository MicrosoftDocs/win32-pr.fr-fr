---
description: Provoque la génération d’un événement à une date spécifique à un moment donné.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918840"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_AbsoluteTimerInstruction, classe

La classe système **\_ \_ AbsoluteTimerInstruction** provoque la génération d’un événement à une date spécifique à un moment donné. Un consommateur d’événements s’inscrit pour recevoir un événement de minuteur absolu en créant une instance de cette classe. L’événement est généré une fois.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ AbsoluteTimerInstruction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ AbsoluteTimerInstruction** possède les propriétés suivantes.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Chaîne de longueur fixe au [format DMTF](date-and-time-format.md) qui spécifie le moment où le minuteur se déclenche.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’événement du minuteur se produit si WMI ne peut pas le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible. Si la **valeur est true**, l’événement ne se produit pas. La valeur par défaut est **false**. Lorsque WMI ou le consommateur devient disponible, un événement de notification est généré et reçu. Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

<dt>

FALSE
</dt> <dd>

Lorsque WMI ou le consommateur redevient disponible, un événement de notification est généré et reçu.

</dd> <dt>

TRUE
</dt> <dd>

L’événement du minuteur ne se produit pas si WMI n’est pas disponible pour le générer à l’intervalle de temps approprié, ou si le consommateur qui demande à recevoir l’événement n’est pas disponible.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Chaîne unique assignée par l’utilisateur qui identifie un événement de minuteur spécifique. Pour éviter les conflits de noms avec d’autres identificateurs de minuterie, la forme de chaîne d’un GUID de style d’environnement d’ordinateur distribué peut être utilisée. Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ AbsoluteTimerInstruction** est dérivée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

WMI génère l’événement de minuteur absolu en créant une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Réception d’événements chronométrés ou répétitifs](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

