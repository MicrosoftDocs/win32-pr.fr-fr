---
description: La méthode Exit signale que le thread de streaming est en cours de fermeture.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: CSourceStream. Exit, méthode (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2c1c0de67eaa1067a4c72f3500674dddef65ddbb11af1b520973120d2df3c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687429"
---
# <a name="csourcestreamexit-method"></a>CSourceStream. Exit, méthode

La `Exit` méthode signale au thread de streaming de se fermer.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ inattendu.

## <a name="remarks"></a>Remarques

La méthode [**CSourceStream :: inactive**](csourcestream-inactive.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




