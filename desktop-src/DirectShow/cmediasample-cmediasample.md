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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095437"
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

## <a name="remarks"></a>Notes 

La classe de base ne modifie pas la valeur **HRESULT** transmise dans le paramètre *PHR* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




