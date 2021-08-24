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
ms.openlocfilehash: af6747eb9ed39a973d795d8701fd9d7afd1b88e9d0b0db577de6a8e963b840bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634349"
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

## <a name="remarks"></a>Remarques

Cette méthode permet à l’allocateur de définir un nouveau pointeur pour l’exemple.

Cette méthode n’est pas disponible par le biais de l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . L’objet qui crée l’exemple peut accéder à cette méthode (via **CMediaSample**), mais les autres objets ne le peuvent pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




