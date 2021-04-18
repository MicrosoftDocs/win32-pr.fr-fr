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
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529008"
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

## <a name="remarks"></a>Notes

Cette méthode affecte la **valeur false** au membre **bFixedSizeSamples** . Les appels suivants à la méthode [**CMediaType :: GetSampleSize**](cmediatype-getsamplesize.md) retournent zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




