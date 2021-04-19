---
description: La méthode SampleProps récupère les propriétés de l’exemple le plus récent dans une structure de \_ Propriétés am SAMPLE2 \_ .
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Méthode CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521760"
---
# <a name="cbaseinputpinsampleprops-method"></a>Méthode CBaseInputPin. SampleProps

La `SampleProps` méthode récupère les propriétés de l’exemple le plus récent dans une structure [**de \_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="syntax"></a>Syntaxe


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’adresse de la variable membre [**CBaseInputPin :: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




