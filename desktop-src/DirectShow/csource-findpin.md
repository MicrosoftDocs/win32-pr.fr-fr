---
description: 'Méthode CSource. FindPin : la méthode FindPin récupère le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
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
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010042"
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

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un code confidentiel avec cet identificateur.<br/> |



 

## <a name="remarks"></a>Notes

Le premier pin est toujours nommé « 1 »; le deuxième pin est nommé « 2 ». et ainsi de suite. Pour plus d’informations, consultez [**CSourceStream :: QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




