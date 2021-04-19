---
description: Événement de suivi de la gestion de la mémoire pour une opération de réallocation du tas.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Événement ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524637"
---
# <a name="etw_heap_event_realloc-event"></a>\_Événement de \_ réallocation du tas ETW \_

L' **événement \_ \_ \_ realloc du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération de réallocation du tas.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle du tas dans lequel la mémoire a été allouée. Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Nouvelle adresse de la mémoire qui a été allouée.

</dd> <dt>

*OldAddress* 
</dt> <dd>

Ancienne adresse de la mémoire précédemment allouée.

</dd> <dt>

*NewSize* 
</dt> <dd>

Nouvelle taille en octets allouée à partir du tas.

</dd> <dt>

*OldSize* 
</dt> <dd>

Ancienne taille en octets précédemment allouée à partir du tas.

</dd> <dt>

*Source* 
</dt> <dd>

Source de la mémoire que l’allocateur utilise pour l’allocation du tas.

Le tableau suivant répertorie les valeurs possibles pour le paramètre *source* , telles qu’elles sont définies dans le fichier d’en-tête *ntetw. h* :



| Valeur                                                                                                                                                                                                                                                                               | Signification                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**Mémoire \_ À \_ partir de**</dt> <dt>1</dt> </dl>                                       | Mémoire de la liste des.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**Mémoire \_ À partir de \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Mémoire à partir du segment de fragmentation faible.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**Mémoire \_ À partir de \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Mémoire à partir du chemin de code principal.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Mémoire \_ de \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Mémoire du c lent.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Mémoire \_ DE \_ 5 non valide**</dt> <dt></dt> </dl>                                             | Mémoire qui n’était pas valide.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Mémoire \_ À partir du \_ \_ segment segment**</dt> <dt>6</dt> </dl>                             | Cette valeur est réservée à une utilisation ultérieure et n’est jamais retournée.<br/> |



 

</dd> </dl>

Cet événement n’a pas de paramètres.

## <a name="remarks"></a>Notes

L’événement de réallocation d' **\_ événement du tas \_ \_ ETW** est consigné sur toutes les réallocations de tas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de suivi de gestion de la mémoire](memory-management-tracing-events.md)
</dt> </dl>

 

 
