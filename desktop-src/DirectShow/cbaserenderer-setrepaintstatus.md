---
description: La méthode SetRepaintStatus active ou désactive les événements de redessin.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Méthode CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542767"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Méthode CBaseRenderer. SetRepaintStatus

La `SetRepaintStatus` méthode active ou désactive les événements de redessin.

## <a name="syntax"></a>Syntaxe


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bRepaint* 
</dt> <dd>

Valeur booléenne indiquant si les événements de redessination sont activés. Si la **valeur est true**, le filtre envoie les événements de [**\_ redessin ce**](ec-repaint.md) au gestionnaire de graphes de filtre. Dans le cas contraire, il n’enverra pas d' \_ événements de REDESSIN ce.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode garantit que le gestionnaire de graphes de filtre n’est pas submergé d' \_ événements EC REpains redondants. Une fois que le filtre a envoyé un événement de [**\_ redessin ce**](ec-repaint.md) , il appelle cette méthode avec la valeur **true**. Le filtre n’envoie pas d’événements de redessin EC supplémentaires tant qu’il n’a pas \_ reçu plus de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




