---
description: 'Méthode CTransformOutputPin. CurrentMediaType : la méthode CurrentMediaType récupère le type de média pour la connexion de code confidentiel actuelle.'
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
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224716"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>Méthode CTransformOutputPin. CurrentMediaType

La `CurrentMediaType` méthode récupère le type de média pour la connexion de code confidentiel actuelle.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une référence à la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




