---
description: 'Méthode CSourceSeeking. GetDuration : la méthode GetDuration récupère la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Méthode CSourceSeeking. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098767"
---
# <a name="csourceseekinggetduration-method"></a>Méthode CSourceSeeking. GetDuration

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

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Valeur de pointeur **null**<br/> |



 

## <a name="remarks"></a>Notes 

La durée est spécifiée par la variable membre [**CSourceSeeking :: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




