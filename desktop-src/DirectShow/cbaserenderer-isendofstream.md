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
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111301"
---
# <a name="cbaserendererisendofstream-method"></a>Méthode CBaseRenderer. IsEndOfStream

La `IsEndOfStream` méthode interroge si la notification de fin de flux a été reçue.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’indicateur [**CBaseRenderer :: m \_ bEOS**](cbaserenderer-m-beos.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




