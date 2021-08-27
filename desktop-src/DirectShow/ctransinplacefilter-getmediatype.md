---
description: 'Méthode CTransInPlaceFilter. GetMediaType : la méthode GetMediaType récupère un type de média préféré pour la broche de sortie.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Méthode CTransInPlaceFilter. GetMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079299"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>Méthode CTransInPlaceFilter. GetMediaType

La `GetMediaType` méthode récupère un type de média par défaut pour la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPosition* 
</dt> <dd>

Valeur d’index de base zéro.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ inattendu.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) . Dans la classe **CTransInPlaceFilter** , chaque pin appelle le code PIN connecté opposé pour énumérer les types de média préférés. La broche d’entrée appelle la broche d’entrée du filtre en aval, et la broche de sortie appelle la broche de sortie du filtre en amont. Par conséquent, la méthode du filtre `GetMediaType` n’est jamais appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




