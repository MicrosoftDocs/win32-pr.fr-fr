---
description: File d’attente de l’exemple de support.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Membre COutputQueue :: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537513"
---
# <a name="coutputqueuem_list-member"></a>COutputQueue :: m \_ List, membre

File d’attente de l’exemple de support.

## <a name="syntax"></a>Syntaxe


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Notes

Cette variable membre est un pointeur vers un objet [**CGenericList**](cgenericlist.md) qui contient des pointeurs [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Le type **CSampleList** est défini comme suit :

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




