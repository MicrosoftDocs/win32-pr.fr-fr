---
description: La méthode StreamingThreadUsingOutputPin détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Méthode CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526406"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Méthode CDynamicOutputPin. StreamingThreadUsingOutputPin

La méthode StreamingThreadUsingOutputPin détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si un thread effectue une opération de diffusion en continu sur le code confidentiel. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Si des threads ont été retournés avec succès à partir de la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) et n’ont pas effectué d’appel correspondant à la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , cette méthode retourne **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




