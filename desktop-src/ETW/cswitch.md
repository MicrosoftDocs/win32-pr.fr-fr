---
description: Cette classe est la classe de type d’événement pour les événements de changement de contexte. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: CSwitch, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007440"
---
# <a name="cswitch-class"></a>CSwitch, classe

Cette classe est la classe de type d’événement pour les événements de changement de contexte.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a>Membres

La classe **CSwitch** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CSwitch** possède les propriétés suivantes.

<dl> <dt>

**NewThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Nouvel ID de thread après le commutateur.

</dd> <dt>

**NewThreadPriority**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Priorité de thread du nouveau thread.

</dd> <dt>

**NewThreadWaitTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (11), format ("x")
</dt> </dl>

Délai d’attente pour le nouveau thread.

</dd> <dt>

**OldThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

ID de thread précédent.

</dd> <dt>

**OldThreadPriority**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Priorité de thread du thread précédent.

</dd> <dt>

**OldThreadState**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9)
</dt> </dl>

État du thread précédent. Les valeurs d’État possibles sont les suivantes :

| State | Description                                   |
|-------|-----------------------------------------------|
| 0     | Initialized                                   |
| 1     | Ready                                         |
| 2     | Exécution en cours                                       |
| 3     | Standby                                       |
| 4     | Terminé                                    |
| 5     | En attente                                       |
| 6     | Transition                                    |
| 7     | DeferredReady (ajouté pour le serveur Windows 2003) |



 

</dd> <dt>

**OldThreadWaitIdealProcessor**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10), format ("x")
</dt> </dl>

Délai d’attente idéal du thread précédent.

</dd> <dt>

**OldThreadWaitMode**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8)
</dt> </dl>

Mode d’attente pour le thread précédent. Les valeurs possibles sont les suivantes :

| State | Description |
|-------|-------------|
| 0     | Kernelmode.  |
| 1     | UserMode    |



 

</dd> <dt>

**OldThreadWaitReason**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7)
</dt> </dl>

Raison de l’attente du thread précédent. Les valeurs possibles sont les suivantes :

| State | Description       |
|-------|-------------------|
| 0     | Executive         |
| 1     | FreePage          |
| 2     | Du pagein.            |
| 3     | PoolAllocation    |
| 4     | DelayExecution    |
| 5     | Interrompu         |
| 6     | UserRequest       |
| 7     | WrExecutive       |
| 8     | WrFreePage        |
| 9     | WrPageIn          |
| 10    | WrPoolAllocation  |
| 11    | WrDelayExecution  |
| 12    | WrSuspended       |
| 13    | WrUserRequest     |
| 14    | WrEventPair       |
| 15    | WrQueue           |
| 16    | WrLpcReceive      |
| 17    | WrLpcReply        |
| 18    | WrVirtualMemory   |
| 19    | WrPageOut         |
| 20    | WrRendezvous      |
| 21    | WrKeyedEvent      |
| 22    | WrTerminated      |
| 23    | WrProcessInSwap   |
| 24    | WrCpuRateControl  |
| 25    | WrCalloutStack    |
| 26    | WrKernel          |
| 27    | WrResource        |
| 28    | WrPushLock        |
| 29    | WrMutex           |
| 30    | WrQuantumEnd      |
| 31    | WrDispatchInt     |
| 32    | WrPreempted       |
| 33    | WrYieldExecution  |
| 34    | WrFastMutex       |
| 35    | WrGuardedMutex    |
| 36    | WrRundown         |
| 37    | MaximumWaitReason |



 

</dd> <dt>

**PreviousCState**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

Index de l’État C qui a été utilisé pour la dernière fois par le processeur. La valeur 0 représente l’état d’inactivité le plus clair avec des valeurs supérieures représentant des États C plus profonds.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (12)
</dt> </dl>

Réservé.

</dd> <dt>

**SpareByte**
</dt> <dd> <dl> <dt>

Type de données : **sint8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6)
</dt> </dl>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces événements produisent un volume élevé d’événements.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




