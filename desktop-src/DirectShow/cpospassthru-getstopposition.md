---
description: 'La méthode GetStopPosition récupère l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetStopPosition.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Méthode CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539257"
---
# <a name="cpospassthrugetstopposition-method"></a>Méthode CPosPassThru. GetStopPosition

La `GetStopPosition` méthode récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux. Cette méthode implémente la méthode [**IMediaSeeking :: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure d’arrêt, en unités du format d’heure actuel.

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
</dt> </dl>

 

 




