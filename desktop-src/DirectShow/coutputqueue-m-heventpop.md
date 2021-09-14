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
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195587"
---
# <a name="coutputqueuem_heventpop-member"></a>COutputQueue :: m \_ hEventPop, membre

Événement facultatif signalé chaque fois que l’objet supprime un échantillon de la file d’attente. La valeur est initialement **null**. Appelez la méthode [**COutputQueue :: SetPopEvent**](coutputqueue-setpopevent.md) pour spécifier un handle d’événement.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




