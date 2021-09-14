---
description: 'Méthode CPosPassThru. IsFormatSupported : la méthode IsFormatSupported détermine si un format d’heure spécifié est pris en charge. Cette méthode implémente la méthode IMediaSeeking :: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Méthode CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010070"
---
# <a name="cpospassthruisformatsupported-method"></a>Méthode CPosPassThru. IsFormatSupported

La `IsFormatSupported` méthode détermine si un format d’heure spécifié est pris en charge. Cette méthode implémente la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers un GUID de format d’heure.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Spécifications



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

 

 




