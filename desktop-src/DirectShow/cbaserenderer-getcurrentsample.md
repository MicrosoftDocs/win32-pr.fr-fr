---
description: La méthode GetCurrentSample récupère l’exemple actuel.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Méthode CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544453"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Méthode CBaseRenderer. GetCurrentSample

La `GetCurrentSample` méthode récupère l’exemple actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple, ou **null** si aucun échantillon n’est disponible.

## <a name="remarks"></a>Notes

À moins que la méthode ne retourne la **valeur null**, la méthode appelle **AddRef** sur le pointeur [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) avant de la retourner. L’appelant doit libérer le pointeur. (Par implication, vous devez affecter la valeur de retour à une variable, afin de pouvoir la libérer ultérieurement.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




