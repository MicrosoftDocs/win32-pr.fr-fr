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
ms.openlocfilehash: 9544a5f35c42fcf65bff58ad63d6f22bdd4dd817ae91951b01ffe122bce50c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954018"
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

## <a name="remarks"></a>Remarques

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

 

 




