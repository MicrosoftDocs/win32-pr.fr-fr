---
description: La méthode pause signale au thread de streaming qu’il devient actif.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Méthode CSourceStream. pause (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079309"
---
# <a name="csourcestreampause-method"></a>CSourceStream. pause, méthode

La `Pause` méthode signale au thread de streaming qu’il devient actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ inattendu.

## <a name="remarks"></a>Remarques

La méthode [**CSourceStream :: active**](csourcestream-active.md) appelle cette méthode. Quand la méthode [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md) reçoit cette demande, elle appelle la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




