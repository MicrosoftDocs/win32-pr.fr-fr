---
description: La méthode IsUsingDefaultSource détermine si le convertisseur utilise la fenêtre source par défaut.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Méthode CBaseControlVideo. IsUsingDefaultSource (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545689"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>Méthode CBaseControlVideo. IsUsingDefaultSource

La `IsUsingDefaultSource` méthode détermine si le convertisseur utilise la fenêtre source par défaut.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le convertisseur utilise la source par défaut ; sinon, retourne s \_ false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




