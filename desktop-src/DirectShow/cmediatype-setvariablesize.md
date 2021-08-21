---
description: La méthode SetVariableSize spécifie que les exemples n’ont pas de taille fixe.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Méthode CMediaType. SetVariableSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073963"
---
# <a name="cmediatypesetvariablesize-method"></a>Méthode CMediaType. SetVariableSize

La `SetVariableSize` méthode spécifie que les exemples n’ont pas de taille fixe.

## <a name="syntax"></a>Syntaxe


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode affecte la **valeur false** au membre **bFixedSizeSamples** . Les appels suivants à la méthode [**CMediaType :: GetSampleSize**](cmediatype-getsamplesize.md) retournent zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




