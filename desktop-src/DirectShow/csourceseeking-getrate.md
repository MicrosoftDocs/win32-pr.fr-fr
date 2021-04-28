---
description: 'Méthode CSourceSeeking. GetRate : la méthode GetRate récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Méthode CSourceSeeking. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085227"
---
# <a name="csourceseekinggetrate-method"></a>Méthode CSourceSeeking. GetRate

La `GetRate` méthode récupère la vitesse de lecture. Cette méthode implémente la méthode [**IMediaSeeking :: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdRate* 
</dt> <dd>

Pointeur vers une variable qui reçoit la vitesse de lecture.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Valeur de pointeur **null**<br/> |



 

## <a name="remarks"></a>Notes 

La vitesse de lecture est spécifiée par la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




