---
description: 'La méthode ConvertTimeFormat convertit d’un format d’heure en un autre. Cette méthode implémente la méthode IMediaSeeking :: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Méthode CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526331"
---
# <a name="cpospassthruconverttimeformat-method"></a>Méthode CPosPassThru. ConvertTimeFormat

La `ConvertTimeFormat` méthode convertit d’un format d’heure en un autre. Cette méthode implémente la méthode [**IMediaSeeking :: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTarget* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure convertie.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Pointeur vers le GUID du format d’heure du format cible. Si la **valeur est null**, le format actuel est utilisé.

</dd> <dt>

*Source* 
</dt> <dd>

Valeur de temps à convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Pointeur vers le GUID du format d’heure du format à convertir. Si la **valeur est null**, le format actuel est utilisé.

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

 

 




