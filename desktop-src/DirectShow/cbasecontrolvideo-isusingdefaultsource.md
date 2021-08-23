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
ms.openlocfilehash: dce06ffa85b3736eca17f1ecb8303a41afb142fcc8b0d369e1f264a0cf47b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955208"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




