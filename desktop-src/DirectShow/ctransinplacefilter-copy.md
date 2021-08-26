---
description: La méthode Copy copie un exemple de support.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: CTransInPlaceFilter. Copy, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10a7a2927789ffe49d37912862580222f0ed06d9648b6312cbb044e357d6e61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053519"
---
# <a name="ctransinplacefiltercopy-method"></a>CTransInPlaceFilter. Copy, méthode

La `Copy` méthode copie un échantillon de média.

## <a name="syntax"></a>Syntaxe


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSource* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface **IMediaSample** sur le nouvel exemple.

## <a name="remarks"></a>Remarques

Cette méthode récupère une mémoire tampon vide à partir de l’allocateur en aval. Elle copie tous les exemples de propriétés de *pSource* dans le nouvel exemple, ainsi que les données réelles dans l’exemple. Si le filtre utilise deux allocations, il appelle cette méthode pour copier des données dans les mémoires tampons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




