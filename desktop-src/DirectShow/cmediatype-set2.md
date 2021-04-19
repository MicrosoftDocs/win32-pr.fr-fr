---
description: La méthode Set définit le type de média à partir d’un autre type de média.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType. Set, méthode (mtype. h)-mtype [ref], paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106540131"
---
# <a name="cmediatypeset-method-mtypeh"></a>CMediaType. Set, méthode (mtype. h)

La `Set` méthode définit le type de média à partir d’un autre type de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtype* \[ Réf\]
</dt> <dd>

Référence à une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode copie l’intégralité du type de média à partir de *mtype*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




