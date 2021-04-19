---
description: 'La méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode IMediaSeeking :: SetTimeFormat.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Méthode CPosPassThru. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533087"
---
# <a name="cpospassthrusettimeformat-method"></a>Méthode CPosPassThru. SetTimeFormat

La méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers un GUID de format d’heure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> <dt>

[**GUID de format d’heure**](time-format-guids.md)
</dt> </dl>

 

 




