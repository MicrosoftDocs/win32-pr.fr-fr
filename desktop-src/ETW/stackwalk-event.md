---
description: Cette classe est la classe de type d’événement pour les événements de suivi de pile.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 672d8fc609c14a43ca2692b5cf8a46356a00cccb9c06371e515bc102706c3638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069699"
---
# <a name="stackwalk_event-class"></a>\_Classe d’événements StackWalk

Cette classe est la classe de type d’événement pour les événements de suivi de pile.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>Membres

La classe d' **\_ événements StackWalk** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ événements StackWalk** a ces propriétés.

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1)
</dt> </dl>

Horodatage de l’événement d’origine à partir de l’en-tête de l’événement. Utilisez cet horodatage pour faire correspondre la pile à un événement.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), pointeur
</dt> </dl>

Adresse de l’appel.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (195), pointeur
</dt> </dl>

Adresse de l’appel.

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

Identificateur de processus de l’événement d’origine.

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Identificateur de thread de l’événement d’origine.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez que la classe n’affiche pas toutes les propriétés **Stack * n*** qui existent entre **Stack1** et **Stack192**. Utilisez la taille de l’événement pour déterminer le nombre de propriétés de **pile * n*** qui contiennent des adresses valides.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 




