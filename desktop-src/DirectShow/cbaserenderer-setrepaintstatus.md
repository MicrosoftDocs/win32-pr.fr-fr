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
ms.openlocfilehash: 748d0091bd3d2eae11773a9f94b62ceeb92b2d3ca64049f1a1981e38bf222e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016847"
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

## <a name="remarks"></a>Remarques

Cette méthode garantit que le gestionnaire de graphes de filtre n’est pas submergé d' \_ événements EC REpains redondants. Une fois que le filtre a envoyé un événement de [**\_ redessin ce**](ec-repaint.md) , il appelle cette méthode avec la valeur **true**. Le filtre n’envoie pas d’événements de redessin EC supplémentaires tant qu’il n’a pas \_ reçu plus de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




