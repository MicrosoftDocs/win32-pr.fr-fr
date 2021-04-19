---
description: La méthode OnThreadStartPlay est appelée au début de la méthode CSourceStream ::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Méthode CSourceStream. OnThreadStartPlay (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541586"
---
# <a name="csourcestreamonthreadstartplay-method"></a>Méthode CSourceStream. OnThreadStartPlay

La `OnThreadStartPlay` méthode est appelée au début de la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode n’a aucun effet dans la classe de base ; elle est disponible pour la substitution de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




