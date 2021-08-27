---
description: 'Tableau d’exemples de taille COutputQueue :: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membre COutputQueue :: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103149"
---
# <a name="coutputqueuem_ppsamples-member"></a>COutputQueue :: m \_ ppSamples, membre

Tableau d’exemples de taille [**COutputQueue :: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Syntaxe


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Notes

Le thread de travail extrait des exemples de la file d’attente et les place dans ce tableau. Il passe le tableau à la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) . Si l’objet n’utilise pas de thread de travail, l’objet place des exemples directement dans ce tableau. La variable de membre de [**\_ liste COutputQueue :: m**](coutputqueue-m-list.md) contient la file d’attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




