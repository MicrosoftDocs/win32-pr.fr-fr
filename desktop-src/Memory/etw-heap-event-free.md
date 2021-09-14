---
description: Événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: Événement ETW_HEAP_EVENT_FREE (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094166"
---
# <a name="etw_heap_event_free-event"></a>Événement \_ libre du tas ETW \_ \_

L' **événement \_ \_ \_ libre du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle du tas dans lequel la mémoire a été allouée. Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.

</dd> <dt>

*Adresse* 
</dt> <dd>

Adresse de la mémoire libérée.

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

## <a name="remarks"></a>Notes

L' **événement \_ \_ \_ libre du tas ETW** est enregistré dans toutes les opérations libres du tas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de suivi de gestion de la mémoire](memory-management-tracing-events.md)
</dt> </dl>

 

 
