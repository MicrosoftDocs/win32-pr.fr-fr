---
description: Événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Événement ETW_HEAP_EVENT_ALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318425"
---
# <a name="etw_heap_event_alloc-event"></a>\_ \_ Événement Alloc du tas ETW \_

L' **événement \_ \_ \_ Alloc du tas ETW** est un événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle du tas dans lequel la mémoire a été allouée. Il s’agit du tas handle d’une application transmise à la fonction [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) lorsque la mémoire a été allouée.

</dd> <dt>

*Taille* 
</dt> <dd>

Taille, en octets, allouée à partir du tas.

</dd> <dt>

*Adresse* 
</dt> <dd>

Adresse de la mémoire qui a été allouée.

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
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Mémoire \_ de \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Mémoire à partir du chemin d’accès lent.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Mémoire \_ DE \_ 5 non valide**</dt> <dt></dt> </dl>                                             | Mémoire qui n’était pas valide.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Mémoire \_ À partir du \_ \_ segment segment**</dt> <dt>6</dt> </dl>                             | Cette valeur est réservée à une utilisation ultérieure et n’est jamais retournée.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

L' **événement \_ \_ \_ Alloc du tas ETW** est enregistré sur toutes les allocations de tas.

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

 

 
