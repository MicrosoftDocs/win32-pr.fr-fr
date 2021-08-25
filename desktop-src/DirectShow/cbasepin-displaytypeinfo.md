---
description: La méthode DisplayTypeInfo affiche les informations sur le type de média pendant le débogage.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Méthode CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10b4535950a46fa55aba0ea7d808a075186f074cc829be0d3225dc887512ad47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916449"
---
# <a name="cbasepindisplaytypeinfo-method"></a>Méthode CBasePin. DisplayTypeInfo

La `DisplayTypeInfo` méthode affiche les informations sur le type de média pendant le débogage.

## <a name="syntax"></a>Syntaxe


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Ignoré.

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Dans les versions Debug, cette méthode appelle la fonction [**DbgLog**](dbglog.md) pour afficher le type de média spécifié. Dans les versions commerciales, cette méthode n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




