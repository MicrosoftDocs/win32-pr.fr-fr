---
description: La méthode FindPinNumber récupère le numéro d’un pin spécifié sur le filtre.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Méthode CSource. FindPinNumber (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8082cb19b275f8ebfebd0f2c9beda0eb9854699bf92f29e9d994ee4391e628f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084099"
---
# <a name="csourcefindpinnumber-method"></a>Méthode CSource. FindPinNumber

La `FindPinNumber` méthode récupère le numéro d’un pin spécifié sur le filtre.

## <a name="syntax"></a>Syntaxe


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le numéro de code confidentiel, ou 1 si le code PIN est introuvable sur ce filtre. Le premier code PIN est numéroté à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




