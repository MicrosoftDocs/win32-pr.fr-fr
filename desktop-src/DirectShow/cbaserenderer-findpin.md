---
description: La méthode FindPin récupère le code confidentiel avec l’identificateur spécifié.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Méthode CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530328"
---
# <a name="cbaserendererfindpin-method"></a>Méthode CBaseRenderer. FindPin

La `FindPin` méthode récupère le code confidentiel avec l’identificateur spécifié.

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

Pointeur vers une chaîne de caractères larges se terminant par null qui identifie le code confidentiel. Doit être L "in".

</dd> <dt>

*ppPin* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin. Si la méthode échoue, *\* ppPin* a la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Opération réussie.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Introuvable.<br/>                 |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: FindPin**](cbasefilter-findpin.md) . La seule broche du filtre (la broche d’entrée) est nommée « in ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




