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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999319"
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

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Introuvable.<br/>                 |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: FindPin**](cbasefilter-findpin.md) . La seule broche du filtre (la broche d’entrée) est nommée « in ».

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




