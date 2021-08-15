---
description: La méthode AbortPlayback est utilisée pour signaler une erreur de diffusion en continu. elle envoie un \_ événement EC ERRORABORT au gestionnaire de Graph de filtre et envoie une notification de fin de flux en aval.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Méthode CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821934"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Méthode CVideoTransformFilter. AbortPlayback

La `AbortPlayback` méthode est utilisée pour signaler une erreur de diffusion en continu. elle envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de Graph de filtre et envoie une notification de fin de flux en aval.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*heure(s)* 
</dt> <dd>

Valeur **HRESULT** de l’opération qui a échoué. Cette valeur est utilisée comme premier paramètre d’événement pour l' \_ événement EC ERRORABORT.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du paramètre *HR* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




