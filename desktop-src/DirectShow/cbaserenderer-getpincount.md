---
description: 'Méthode CBaseRenderer. GetPinCount : la méthode GetPinCount récupère le nombre de broches.'
ms.assetid: 518de15d-2ecf-425e-b4cd-14aaaf938417
title: Méthode CBaseRenderer. GetPinCount (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdd646458bb10287e1a76ffed897f1ea039e1b047ccf14d10aeb990ebfc74622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403448"
---
# <a name="cbaserenderergetpincount-method"></a>Méthode CBaseRenderer. GetPinCount

La `GetPinCount` méthode récupère le nombre de broches.

## <a name="syntax"></a>Syntaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Renvoie 1.

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md) , qui est virtuelle pure dans la classe **CBaseFilter** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




