---
description: 'Classe Thread_V2_TypeGroup1 : cette classe est la classe de type d’événement pour les événements de début et de fin de thread. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Classe Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105657"
---
# <a name="thread_v2_typegroup1-class"></a>\_ \_ Classe TypeGroup1 du thread v2

Cette classe est la classe de type d’événement pour les événements de début et de fin de thread.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ TypeGroup1 du thread v2** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ TypeGroup1 du thread v2** a ces propriétés.

<dl> <dt>

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

StartAddr
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), pointeur
</dt> </dl>

Adresse mémoire à laquelle le suivi démarre.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




