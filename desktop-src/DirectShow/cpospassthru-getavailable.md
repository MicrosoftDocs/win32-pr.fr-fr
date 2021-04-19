---
description: 'La méthode GetAvailable récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode IMediaSeeking :: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Méthode CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542551"
---
# <a name="cpospassthrugetavailable-method"></a>Méthode CPosPassThru. GetAvailable

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

Pointeur vers une variable qui reçoit l’heure la plus précoce pour une recherche efficace.

</dd> <dt>

*Plaque* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure la plus récente pour une recherche efficace.

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

 

 




