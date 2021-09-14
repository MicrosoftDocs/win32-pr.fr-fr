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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006795"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Méthode CDynamicOutputPin. StreamingThreadUsingOutputPin

La méthode StreamingThreadUsingOutputPin détermine si un thread effectue une opération de diffusion en continu sur le code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si un thread effectue une opération de diffusion en continu sur le code confidentiel. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

Si des threads ont été retournés avec succès à partir de la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) et n’ont pas effectué d’appel correspondant à la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , cette méthode retourne **true**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




