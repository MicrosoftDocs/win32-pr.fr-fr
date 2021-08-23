---
description: Charge les données du filtre à partir d’un flux donné.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: CPersistStream. Load, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d65ff2d2ba95f66e6153aa78a9ce376ed144ac24ce8945c1fbc678e9f6894802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813349"
---
# <a name="cpersiststreamload-method"></a>CPersistStream. Load, méthode

Charge les données du filtre à partir d’un flux donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStm* 
</dt> <dd>

Pointeur vers le flux à partir duquel le chargement doit être effectué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode **IPersistStream :: Load** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




