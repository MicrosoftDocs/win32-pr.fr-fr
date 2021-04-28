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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085157"
---
# <a name="ctransformfilterbeginflush-method"></a>Méthode CTransformFilter. BeginFlush

La `BeginFlush` méthode commence une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes 

Au démarrage d’une opération de vidage, la méthode [**CTransformInputPin :: BeginFlush**](ctransforminputpin-beginflush.md) de la broche d’entrée appelle cette méthode. Cette méthode passe l' `BeginFlush` appel en aval.

Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente pendant une opération de vidage. Cela peut être effectué dans la `BeginFlush` méthode ou dans la méthode [**EndFlush**](ctransformfilter-endflush.md) . Toutefois, Notez que les appels à `BeginFlush` ne sont pas synchronisés avec le thread de streaming. Si la `BeginFlush` méthode ignore les données mises en file d’attente, le filtre doit veiller à ne pas traiter davantage de données entre les `BeginFlush` appels de **EndFlush** et. Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




