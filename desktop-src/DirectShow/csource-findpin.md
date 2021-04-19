---
description: 'La méthode FindPin récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Méthode CSource. FindPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535853"
---
# <a name="csourcefindpin-method"></a>Méthode CSource. FindPin

La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui identifie le code confidentiel.

</dd> <dt>

*ppPin* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin. Si la méthode échoue, \* *ppPin* a la valeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Opération réussie.<br/>                                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un code confidentiel avec cet identificateur.<br/> |



 

## <a name="remarks"></a>Notes

Le premier pin est toujours nommé « 1 »; le deuxième pin est nommé « 2 ». et ainsi de suite. Pour plus d’informations, consultez [**CSourceStream :: QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




