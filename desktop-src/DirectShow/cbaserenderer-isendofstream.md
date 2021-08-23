---
description: La méthode IsEndOfStream interroge si la notification de fin de flux a été reçue.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Méthode CBaseRenderer. IsEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50aab34fe73f617409ae3f1e33d132a45f8ea771722c42629d9f0e3df5ebb115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872309"
---
# <a name="cbaserendererisendofstream-method"></a>Méthode CBaseRenderer. IsEndOfStream

La `IsEndOfStream` méthode interroge si la notification de fin de flux a été reçue.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur [**CBaseRenderer :: m \_ bEOS**](cbaserenderer-m-beos.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




