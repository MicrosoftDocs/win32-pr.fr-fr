---
description: Méthode constructeur CMediaSample. CMediaSample.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Constructeur CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634689"
---
# <a name="cmediasamplecmediasample-constructor"></a>Constructeur CMediaSample. CMediaSample

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Pointeur vers l’objet [**CBaseAllocator**](cbaseallocator.md) qui a créé cet exemple.

</dd> <dt>

*phr* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon allouée par l’appelant, de la *longueur* de la taille.

</dd> <dt>

*length* 
</dt> <dd>

Longueur de la mémoire tampon.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe de base ne modifie pas la valeur **HRESULT** transmise dans le paramètre *PHR* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




