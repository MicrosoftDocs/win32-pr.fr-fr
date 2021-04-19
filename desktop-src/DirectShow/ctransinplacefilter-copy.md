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
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530014"
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

## <a name="remarks"></a>Notes

Cette méthode récupère une mémoire tampon vide à partir de l’allocateur en aval. Elle copie tous les exemples de propriétés de *pSource* dans le nouvel exemple, ainsi que les données réelles dans l’exemple. Si le filtre utilise deux allocations, il appelle cette méthode pour copier des données dans les mémoires tampons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




