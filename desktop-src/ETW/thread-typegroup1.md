---
description: Cette classe est la classe de type d’événement pour les événements de début et de fin de thread. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Classe Thread_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114590"
---
# <a name="thread_typegroup1-class"></a>\_Classe TypeGroup1 du thread

Cette classe est la classe de type d’événement pour les événements de début et de fin de thread.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a>Membres

La classe **thread \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **thread \_ TypeGroup1** a ces propriétés.

<dl> <dt>

Affinité
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), pointeur
</dt> </dl>

Ensemble des processeurs sur lesquels le thread est autorisé à s’exécuter.

</dd> <dt>

BasePriority
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (11)
</dt> </dl>

Priorité du planificateur du thread (consultez la fonction [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) ).

</dd> <dt>

IoPriority
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (13)
</dt> </dl>

Indicateur de priorité d’e/s pour la planification d’IOs généré par le thread.

</dd> <dt>

PagePriority
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (12)
</dt> </dl>

Indicateur de priorité de page mémoire pour les pages mémoire accessibles par le thread.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Identificateur de processus du thread impliqué dans l’événement.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), pointeur
</dt> </dl>

Adresse de base de la pile du thread.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), pointeur
</dt> </dl>

Limite de la pile du thread.

</dd> <dt>

SubProcessTag
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10), format ("x")
</dt> </dl>

Identifie le service si le thread appartient à un service ; Sinon, zéro.

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9), pointeur
</dt> </dl>

Adresse de base du bloc de l’environnement du thread.

</dd> <dt>

ThreadFlags
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (14)
</dt> </dl>

Non utilisé.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

Identificateur de thread du thread impliqué dans l’événement.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), pointeur
</dt> </dl>

Adresse de base de la pile du mode utilisateur du thread.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), pointeur
</dt> </dl>

Limite de la pile du mode utilisateur du thread.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8), pointeur
</dt> </dl>

Adresse de début de la fonction à exécuter par ce thread.

</dd> </dl>

## <a name="remarks"></a>Notes

Les types d’événements DCStart et DCEnd énumèrent les threads en cours d’exécution au moment où la session du noyau démarre et se termine, respectivement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Thread**](thread.md)
</dt> </dl>

 

 
