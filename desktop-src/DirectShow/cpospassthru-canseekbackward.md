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
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540203"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




