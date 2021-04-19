---
description: La méthode EndOfStream est appelée une fois que l’objet remet le dernier échantillon. La classe dérivée doit implémenter cette méthode.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Méthode CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543285"
---
# <a name="cpullpinendofstream-method"></a>Méthode CPullPin. EndOfStream

La `EndOfStream` méthode est appelée une fois que l’objet remet le dernier échantillon. La classe dérivée doit implémenter cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Utilisez cette méthode pour appeler [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur chaque broche d’entrée en aval qui reçoit les données de cet objet. Si la ou les broches de sortie de votre filtre dérivent de [**CBaseOutputPin**](cbaseoutputpin.md), appelez la méthode [**CBaseOutputPin ::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




