---
description: La méthode SetMediaType est appelée lorsque le type de média du pin est défini.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Méthode CBaseRenderer. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540075"
---
# <a name="cbaserenderersetmediatype-method"></a>Méthode CBaseRenderer. SetMediaType

La `SetMediaType` méthode est appelée lorsque le type de média du pin est défini.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: SetMediaType**](crendererinputpin-setmediatype.md) . Cette méthode n’a aucun effet dans la classe de base.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




