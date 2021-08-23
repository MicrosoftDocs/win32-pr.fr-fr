---
description: La méthode IsSpecialSample détermine si les données mises en file d’attente sont des messages de contrôle.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Méthode COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c192196869f86e8d78da2f6b38a661373e115753d99e554f4b7a868eb0b484fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688219"
---
# <a name="coutputqueueisspecialsample-method"></a>Méthode COutputQueue. IsSpecialSample

La `IsSpecialSample` méthode détermine si les données mises en file d’attente sont des messages de contrôle.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers un élément de la file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si *pSample* est un message de contrôle, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La méthode [**COutputQueue :: QueueSample**](coutputqueue-queuesample.md) peut recevoir des messages de contrôle en plus des exemples de supports. Un message de contrôle est une constante définie (castée en un \_ type PTR long) qui indique au thread d’effectuer une action. Les messages de contrôle ne contiennent pas de données multimédias. Pour plus d’informations, consultez **COutputQueue :: QueueSample**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




