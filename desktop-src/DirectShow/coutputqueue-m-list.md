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
ms.openlocfilehash: 3e261116961f23c845ec2e27c6f20748b2c50cd9c036d9bc7d42bfe24b9b4fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087069"
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
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




