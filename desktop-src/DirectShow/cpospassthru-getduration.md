---
description: 'Méthode CPosPassThru. GetDuration : la méthode GetDuration récupère la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Méthode CPosPassThru. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012271"
---
# <a name="cpospassthrugetduration-method"></a>Méthode CPosPassThru. GetDuration

La `GetDuration` méthode récupère la durée du flux. Cette méthode implémente la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDuration* 
</dt> <dd>

Pointeur vers une variable qui reçoit la durée, en unités du format d’heure actuel.

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
</dt> </dl>

 

 




