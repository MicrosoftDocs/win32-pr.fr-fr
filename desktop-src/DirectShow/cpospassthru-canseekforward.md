---
description: 'La méthode CanSeekForward détermine si le flux peut être recherché par progression. Cette méthode implémente la méthode IMediaPosition :: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Méthode CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541344"
---
# <a name="cpospassthrucanseekforward-method"></a>Méthode CPosPassThru. CanSeekForward

La `CanSeekForward` méthode détermine si le flux peut être recherché. Cette méthode implémente la méthode [**IMediaPosition :: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Pointeur vers une variable qui reçoit la valeur OATRUE si le filtre peut effectuer une recherche vers l’avant ou OAFALSE dans le cas contraire.

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

 

 




