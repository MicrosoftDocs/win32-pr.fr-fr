---
description: La méthode EndOfStream indique au filtre qu’aucune donnée supplémentaire n’est attendue à partir de la broche d’entrée.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Méthode CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907629"
---
# <a name="ctransformfilterendofstream-method"></a>Méthode CTransformFilter. EndOfStream

La `EndOfStream` méthode informe le filtre qu’aucune donnée supplémentaire n’est attendue à partir de la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode [**CTransformInputPin :: EndOfStream**](ctransforminputpin-endofstream.md) du code confidentiel d’entrée appelle cette méthode. Cette méthode fournit la notification de fin de flux en aval. Si la classe dérivée utilise un thread de travail pour fournir des exemples de média, elle doit substituer cette méthode et mettre en file d’attente la notification de fin de flux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




