---
description: 'Événement facultatif signalé chaque fois que l’objet supprime un échantillon de la file d’attente. La valeur est initialement NULL. Appelez la méthode COutputQueue :: SetPopEvent pour spécifier un handle d’événement.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membre COutputQueue :: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb401cf9755260c797ebfb382d9f2248d9d04c5f8d9e9b49e319c390de1664c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087209"
---
# <a name="coutputqueuem_heventpop-member"></a>COutputQueue :: m \_ hEventPop, membre

Événement facultatif signalé chaque fois que l’objet supprime un échantillon de la file d’attente. La valeur est initialement **null**. Appelez la méthode [**COutputQueue :: SetPopEvent**](coutputqueue-setpopevent.md) pour spécifier un handle d’événement.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




