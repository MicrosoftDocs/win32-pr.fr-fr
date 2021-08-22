---
description: 'CTransformOutputPin :: m_pPosition objet d’assistance de membre pour passer les commandes de recherche en amont.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membre CTransformOutputPin :: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bfa565d38fa982ea457da13ee9cf08a1d0f2fe8d5ba52ef3c5b86379fc02b509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538159"
---
# <a name="ctransformoutputpinm_pposition-member"></a>CTransformOutputPin :: m \_ pPosition, membre

Objet d’assistance pour passer les commandes de recherche en amont.

## <a name="syntax"></a>Syntaxe


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Notes

Lorsque le code PIN est demandé pour la première fois pour l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , il crée et agrège un objet d’assistance [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




