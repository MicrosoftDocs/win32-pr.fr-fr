---
description: 'La méthode FindPin obtient le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode IBaseFilter :: FindPin.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Méthode CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528529"
---
# <a name="ctransformfilterfindpin-method"></a>Méthode CTransformFilter. FindPin

La méthode **FindPin** obtient le code confidentiel avec l’identificateur spécifié. Cette méthode implémente la méthode [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

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

Chaîne de caractères larges qui contient l’identificateur de code confidentiel.

</dd> <dt>

*ppPin* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin. Si la méthode échoue, `*ppPin` a la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Opération réussie.<br/>                                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>     | Mémoire insuffisante.<br/>                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un code confidentiel avec cet identificateur.<br/> |



 

## <a name="remarks"></a>Notes

> [!IMPORTANT]
> L’implémentation de cette méthode n’appelle pas [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) pour correspondre à l’identificateur de code confidentiel. Au lieu de cela, la méthode suppose que la broche d’entrée est nommée « in » et que la broche de sortie est nommée « out ». Si vous utilisez un autre jeu d’identificateurs de code confidentiel, substituez cette méthode.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




