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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224601"
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

## <a name="return-value"></a>Valeur de retour

Retourne E \_ inattendu.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) . Dans la classe **CTransInPlaceFilter** , chaque pin appelle le code PIN connecté opposé pour énumérer les types de média préférés. La broche d’entrée appelle la broche d’entrée du filtre en aval, et la broche de sortie appelle la broche de sortie du filtre en amont. Par conséquent, la méthode du filtre `GetMediaType` n’est jamais appelée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




