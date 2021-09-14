---
description: La méthode IncremementPinVersion incrémente le numéro de version sur le jeu de broches.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Méthode CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007647"
---
# <a name="cbasefilterincrementpinversion-method"></a>Méthode CBaseFilter. IncrementPinVersion

La `IncremementPinVersion` méthode incrémente le numéro de version sur le jeu de broches.

## <a name="syntax"></a>Syntaxe


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode incrémente la variable membre [**CBaseFilter :: m \_ PinVersion**](cbasefilter-m-pinversion.md) . Si le filtre crée ou détruit dynamiquement des codes confidentiels, appelez cette méthode chaque fois que les codes confidentiels changent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




