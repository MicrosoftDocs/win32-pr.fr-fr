---
description: La méthode OnError est appelée si une erreur se produit pendant la diffusion en continu. La classe dérivée doit implémenter cette méthode.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: CPullPin. OnError, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541429"
---
# <a name="cpullpinonerror-method"></a>CPullPin. OnError, méthode

La `OnError` méthode est appelée si une erreur se produit pendant la diffusion en continu. La classe dérivée doit implémenter cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*heure(s)* 
</dt> <dd>

Spécifie la valeur **HRESULT** retournée par la méthode qui a échoué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’objet appelle cette méthode chaque fois qu’une erreur se produit et arrête le thread d’extraction de données. Le filtre peut utiliser cette méthode pour récupérer les erreurs de diffusion en continu de manière appropriée. Dans la plupart des cas, l’erreur est retournée à partir du filtre en amont. le filtre en amont est donc chargé de les signaler au gestionnaire de graphes de filtre. Si l’erreur se produit à l’intérieur de la méthode [**CPullPin :: Receive**](cpullpin-receive.md) , votre filtre doit envoyer un événement [**EC \_ ERRORABORT**](ec-errorabort.md) . (Voir [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




