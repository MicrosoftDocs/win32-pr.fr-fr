---
description: 'La méthode StartStreaming est appelée lorsque le filtre passe à l’état suspendu. Cette méthode remplace la méthode CTransformFilter :: StartStreaming.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Méthode CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53d448228a650718f8c57d6019dcfb1f3f23f03468e86a77fae167e6481e718c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998469"
---
# <a name="cvideotransformfilterstartstreaming-method"></a>Méthode CVideoTransformFilter. StartStreaming

La `StartStreaming` méthode est appelée lorsque le filtre passe à l’état suspendu. Cette méthode remplace la méthode [**CTransformFilter :: StartStreaming**](ctransformfilter-startstreaming.md) .

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode réinitialise toutes les statistiques de performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




