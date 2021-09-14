---
description: La méthode Init Initialise le thread de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: CSourceStream. Init, méthode (source. h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012233"
---
# <a name="csourcestreaminit-method"></a>CSourceStream. Init, méthode

La `Init` méthode initialise le thread de streaming.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Init();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode doit être la première demande de thread envoyée à la méthode [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md) . La méthode [**CSourceStream :: active**](csourcestream-active.md) appelle cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




