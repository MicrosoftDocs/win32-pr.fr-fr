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
ms.openlocfilehash: 9b654063cc448c8f8e87dcd57442d36b2ed2b2cf2d3135d0ab987c01ff1a7569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983649"
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
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




