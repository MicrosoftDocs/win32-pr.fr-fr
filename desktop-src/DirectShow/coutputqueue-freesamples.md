---
description: La méthode FreeSamples libère tous les échantillons en attente.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Méthode COutputQueue. FreeSamples (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2cc87047d6dc48494fc225b5a0b4c4ad7bcb69f0f7341580f8c48c1440470bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954158"
---
# <a name="coutputqueuefreesamples-method"></a>Méthode COutputQueue. FreeSamples

La `FreeSamples` méthode libère tous les échantillons en attente.

## <a name="syntax"></a>Syntaxe


```C++
void FreeSamples();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode supprime tous les échantillons en attente de la file d’attente et de l’exemple de tableau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




