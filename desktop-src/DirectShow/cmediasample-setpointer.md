---
description: La méthode SetPoint définit le pointeur sur la mémoire tampon.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Méthode CMediaSample. SetPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544072"
---
# <a name="cmediasamplesetpointer-method"></a>CMediaSample. SetPoint, méthode

La `SetPointer` méthode définit le pointeur sur la mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptr* 
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant, de taille *cBytes*.

</dd> <dt>

*cBytes* 
</dt> <dd>

Longueur de la mémoire tampon, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode permet à l’allocateur de définir un nouveau pointeur pour l’exemple.

Cette méthode n’est pas disponible par le biais de l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . L’objet qui crée l’exemple peut accéder à cette méthode (via **CMediaSample**), mais les autres objets ne le peuvent pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




