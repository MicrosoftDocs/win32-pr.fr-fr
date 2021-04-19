---
description: La méthode Init Initialise le thread de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Méthode CSourceStream.Init (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542643"
---
# <a name="csourcestreaminit-method"></a>Méthode CSourceStream.Init

La `Init` méthode initialise le thread de streaming.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Init();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode doit être la première demande de thread envoyée à la méthode [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md) . La méthode [**CSourceStream :: active**](csourcestream-active.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




