---
description: 'La méthode IsUsingTimeFormat détermine si un format d’heure spécifié est le format en cours d’utilisation. Cette méthode implémente la méthode IMediaSeeking :: IsUsingTimeFormat.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Méthode CPosPassThru. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64c240a0b1c269dde57e07e50bcbdbbd4d5d7e03d24a4e6d263662947f3d65de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954008"
---
# <a name="cpospassthruisusingtimeformat-method"></a>Méthode CPosPassThru. IsUsingTimeFormat

La `IsUsingTimeFormat` méthode détermine si un format d’heure spécifié est le format en cours d’utilisation. Cette méthode implémente la méthode [**IMediaSeeking :: IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsUsingTimeFormat(
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> <dt>

[**GUID de format d’heure**](time-format-guids.md)
</dt> </dl>

 

 




