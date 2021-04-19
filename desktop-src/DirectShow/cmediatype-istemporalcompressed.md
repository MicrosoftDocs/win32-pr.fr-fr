---
description: La méthode IsTemporalCompressed détermine si le flux utilise la compression temporelle.
ms.assetid: 06a57655-a304-429d-a150-819072b91016
title: Méthode CMediaType. IsTemporalCompressed (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsTemporalCompressed
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09c9770c23e0cd7f1f5140a5f9b9f18299ddaa23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537792"
---
# <a name="cmediatypeistemporalcompressed-method"></a>Méthode CMediaType. IsTemporalCompressed

La `IsTemporalCompressed` méthode détermine si le flux utilise la compression temporelle.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsTemporalCompressed() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du membre **bTemporalCompression** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




