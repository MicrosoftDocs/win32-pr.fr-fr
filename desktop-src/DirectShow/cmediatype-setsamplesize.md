---
description: La méthode SetSampleSize spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Méthode CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954408"
---
# <a name="cmediatypesetsamplesize-method"></a>Méthode CMediaType. SetSampleSize

La `SetSampleSize` méthode spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable.

## <a name="syntax"></a>Syntaxe


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SZ* 
</dt> <dd>

Taille de l’échantillon, en octets, ou zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la valeur de *SZ* est égale à zéro, le type de média utilise des tailles d’échantillons variables. Dans le cas contraire, la taille de l’échantillon est fixée à *SZ* octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




