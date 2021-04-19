---
description: La méthode AbortPlayback est utilisée pour signaler une erreur de diffusion en continu. Elle envoie un \_ événement EC ERRORABORT au gestionnaire de graphique de filtre et envoie une notification de fin de flux en aval.
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
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525928"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Méthode CVideoTransformFilter. AbortPlayback

La `AbortPlayback` méthode est utilisée pour signaler une erreur de diffusion en continu. Elle envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de graphique de filtre et envoie une notification de fin de flux en aval.

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
| En-tête<br/>  | <dl> <dt>Vtrans. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




