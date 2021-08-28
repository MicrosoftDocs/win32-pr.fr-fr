---
description: génère des événements à intervalles réguliers, comme un \_ message de minuteur WM dans Windows programmation.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640759"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_IntervalTimerInstruction, classe

la classe système **\_ \_ IntervalTimerInstruction** génère des événements à intervalles réguliers, comme un \_ message de minuteur WM dans Windows programmation. Un consommateur d’événements s’inscrit pour recevoir des événements de minuterie d’intervalle en créant une requête d’événement qui fait référence à cette classe. En raison du comportement du système d’exploitation, il n’existe aucune garantie que les événements seront remis à l’intervalle demandé précisément.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ IntervalTimerInstruction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ IntervalTimerInstruction** possède les propriétés suivantes.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](standard-qualifiers.md) (millisecondes)
</dt> </dl>

Nombre de millisecondes entre les déclenchements d’événements.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, cet événement doit être ignoré si l’intervalle est déjà passé. La valeur par défaut est **false**. Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

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

Identificateur unique de cet objet **\_ \_ IntervalTimerInstruction** . Cette propriété est héritée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ IntervalTimerInstruction** est dérivée de [**\_ \_ TimerInstruction**](--timerinstruction.md).

La requête d’événement entrée pour s’inscrire à un événement de minuteur d’intervalle est généralement basée sur la propriété **timerId** . Les événements de notification générés à partir d’un événement intervalle de minuterie contiennent la propriété **NumFirings** qui contient des données reflétant le nombre d’événements déclenchés au moment où les événements n’ont pas pu être reçus. Si **SkipIfPassed** a la valeur **true**, ces informations sont ignorées.

La valeur de la propriété **IntervalBetweenEvents** doit être raisonnablement importante. S’il est trop petit, WMI peut l’ignorer et ne pas générer l’événement en raison de limitations dans certains systèmes d’exploitation.

WMI génère l’événement du minuteur d’intervalle en créant une instance de la classe [**\_ \_ TimerEvent**](--timerevent.md) .

Pour recevoir ces événements de minuterie dans un consommateur d’événements temporaire, exécutez [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) avec la chaîne de requête d’événement suivante :


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Pour recevoir ces événements de minuterie dans un consommateur d’événements permanent, vous devez charger la requête précédente dans un filtre d’événements, définir un consommateur logique et créer une liaison de filtre à consommateur pour le filtre et le consommateur. Pour plus d’informations, consultez [réception d’événements à tout moment](receiving-events-at-all-times.md).

## <a name="examples"></a>Exemples

La déclaration MOF suivante montre comment générer un événement de minuteur Interval avec la propriété Key définie sur « MyEvent » toutes les 10 secondes :


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a>Configuration requise



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
</dt> </dl>

 

