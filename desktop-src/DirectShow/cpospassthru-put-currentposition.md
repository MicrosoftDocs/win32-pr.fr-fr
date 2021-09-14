---
description: La \_ méthode put CurrentPosition définit la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaPosition ::p ut \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Méthode CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010064"
---
# <a name="cpospassthruput_currentposition-method"></a>CPosPassThru. put \_ CurrentPosition, méthode

La `put_CurrentPosition` méthode définit la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*llTime* 
</dt> <dd>

Nouvelle position, en secondes.

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

 

 




