---
description: 'Méthode CTransformFilter. BeginFlush : la méthode BeginFlush commence une opération de vidage.'
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Méthode CTransformFilter. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be20231cf62148e3487aef405735f764bf5c02b7cbaadba3c140728b66bd5391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053859"
---
# <a name="ctransformfilterbeginflush-method"></a>Méthode CTransformFilter. BeginFlush

La `BeginFlush` méthode commence une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Au démarrage d’une opération de vidage, la méthode [**CTransformInputPin :: BeginFlush**](ctransforminputpin-beginflush.md) de la broche d’entrée appelle cette méthode. Cette méthode passe l' `BeginFlush` appel en aval.

Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente pendant une opération de vidage. Cela peut être effectué dans la `BeginFlush` méthode ou dans la méthode [**EndFlush**](ctransformfilter-endflush.md) . Toutefois, Notez que les appels à `BeginFlush` ne sont pas synchronisés avec le thread de streaming. Si la `BeginFlush` méthode ignore les données mises en file d’attente, le filtre doit veiller à ne pas traiter davantage de données entre les `BeginFlush` appels de **EndFlush** et. pour plus d’informations, consultez [Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




