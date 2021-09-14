---
description: La méthode StopStreaming interrompt la diffusion en continu lorsque le filtre sort de l’État en cours d’exécution.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Méthode CBaseRenderer. StopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999741"
---
# <a name="cbaserendererstopstreaming-method"></a>Méthode CBaseRenderer. StopStreaming

La `StopStreaming` méthode interrompt la diffusion en continu lorsque le filtre sort de l’État en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**CBaseRenderer :: OnStopStreaming**](cbaserenderer-onstopstreaming.md) . Cette méthode ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




