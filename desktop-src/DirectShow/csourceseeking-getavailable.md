---
description: 'Méthode CSourceSeeking. GetAvailable : la méthode GetAvailable récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode IMediaSeeking :: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Méthode CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085237"
---
# <a name="csourceseekinggetavailable-method"></a>Méthode CSourceSeeking. GetAvailable

La `GetAvailable` méthode récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode [**IMediaSeeking :: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEarliest* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure la plus précoce pour une recherche efficace. La variable a la valeur zéro.

</dd> <dt>

*Plaque* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure la plus récente pour une recherche efficace. La variable est définie sur la valeur de la variable membre [**CSourceSeeking :: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




