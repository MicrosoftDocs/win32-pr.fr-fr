---
description: 'La méthode CanSeekBackward détermine si le flux peut être recherché en arrière. Cette méthode implémente la méthode IMediaPosition :: CanSeekBackward.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Méthode CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108429"
---
# <a name="cpospassthrucanseekbackward-method"></a>Méthode CPosPassThru. CanSeekBackward

La `CanSeekBackward` méthode détermine si le flux peut être recherché en arrière. Cette méthode implémente la méthode [**IMediaPosition :: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Pointeur vers une variable qui reçoit la valeur OATRUE si le filtre peut effectuer une recherche vers l’arrière, ou OAFALSE dans le cas contraire.

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

 

 




