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
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542657"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




