---
description: La méthode ResetEndOfStream réinitialise les indicateurs de fin de flux.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Méthode CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f65bb1c4a63f1aac004dcbe0e1da267c1f14cf095d9c60e2f68391b50d53a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131429"
---
# <a name="cbaserendererresetendofstream-method"></a>Méthode CBaseRenderer. ResetEndOfStream

La `ResetEndOfStream` méthode réinitialise les indicateurs de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode efface la condition de fin de flux précédente. À ce stade, le filtre peut recevoir de nouvelles données. Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




