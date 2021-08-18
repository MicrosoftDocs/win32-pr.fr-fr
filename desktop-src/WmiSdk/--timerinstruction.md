---
description: Spécifie des instructions sur la façon dont les événements de minuterie doivent être générés pour les consommateurs.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d9081cef3ed58929fa976470b1c567c6accd0f60029f64f28ee7a90d16600d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132012"
---
# <a name="__timerinstruction-class"></a>\_\_TimerInstruction, classe

La classe système abstraite **\_ \_ TimerInstruction** spécifie des instructions sur la façon dont les [événements de minuterie](receiving-a-timed-or-repeating-event.md) doivent être générés pour les consommateurs.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ TimerInstruction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ TimerInstruction** possède les propriétés suivantes.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si un événement de notification sera généré et reçu quand un consommateur sera disponible.

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

Chaîne unique assignée par l’utilisateur qui identifie cet événement de minuteur spécifique. Pour éviter les conflits de noms avec d’autres identificateurs de minuterie, la forme de chaîne d’un GUID de style DCE (Distributed Computer Environment) peut être utilisée. Cette propriété fait partie de l’instance [**\_ \_ TimerEvent**](--timerevent.md) qui représente l’événement.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ TimerInstruction** est dérivée de [**\_ \_ EventGenerator**](--eventgenerator.md).

Les sous-classes **\_ \_ TimerInstruction** sont [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), utilisées par les consommateurs pour s’inscrire à un événement de minuteur absolu, et [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), utilisées pour s’inscrire à un événement de minuteur d’intervalle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

