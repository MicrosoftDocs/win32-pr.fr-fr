---
description: La méthode CurrentMediaType récupère le type de média pour la connexion de code confidentiel actuelle.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Méthode CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528929"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>Méthode CTransformOutputPin. CurrentMediaType

La `CurrentMediaType` méthode récupère le type de média pour la connexion de code confidentiel actuelle.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une référence à la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




