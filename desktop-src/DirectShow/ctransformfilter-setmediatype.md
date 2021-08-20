---
description: La méthode SetMediaType est appelée lorsque le type de média est défini sur l’un des codes confidentiels du filtre.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Méthode CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc9331a532f6748de4e03c6972fdd555e4d5e11516d946bbd131da9acab364c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584939"
---
# <a name="ctransformfiltersetmediatype-method"></a>Méthode CTransformFilter. SetMediaType

La `SetMediaType` méthode est appelée lorsque le type de média est défini sur l’un des codes confidentiels du filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*direction* 
</dt> <dd>

Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant un code confidentiel sur le filtre (entrée ou sortie).

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Les méthodes [**CTransformInputPin :: SetMediaType**](ctransforminputpin-setmediatype.md) et [**CTransformOutputPin :: SetMediaType**](ctransformoutputpin-setmediatype.md) appellent cette méthode quand le type de média d’un pin est défini. Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




