---
description: 'La méthode GetPositions récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaSeeking :: GetPositions.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Méthode CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 948deeb61c5a514bc4bd385c387f10961c21cbaf6090b5e281e1f245e1d23225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108269"
---
# <a name="cpospassthrugetpositions-method"></a>Méthode CPosPassThru. GetPositions

La `GetPositions` méthode récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux. Cette méthode implémente la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position d’arrêt, en unités du format d’heure actuel.

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
</dt> </dl>

 

 




