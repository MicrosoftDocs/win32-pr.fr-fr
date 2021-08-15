---
description: La méthode IsUsingDefaultDestination détermine si le convertisseur utilise la fenêtre de destination par défaut.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Méthode CBaseControlVideo. IsUsingDefaultDestination (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf254ec89cc6804af86c98abaaa0c53ae5f76a25766391529ca4de85bee7d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955218"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a>Méthode CBaseControlVideo. IsUsingDefaultDestination

La `IsUsingDefaultDestination` méthode détermine si le convertisseur utilise la fenêtre de destination par défaut.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si vous utilisez la destination par défaut ; sinon, retourne s \_ false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




