---
description: 'La méthode GetPreroll récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaSeeking :: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Méthode CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b34cd565d246f4401061834b21c005306633e72a6f24cc8367a222b5f3736c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954038"
---
# <a name="cpospassthrugetpreroll-method"></a>Méthode CPosPassThru. GetPreroll

La `GetPreroll` méthode récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode [**IMediaSeeking :: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Pointeur vers une variable qui reçoit le temps de préroll, en unités du format d’heure actuel.

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

 

 




