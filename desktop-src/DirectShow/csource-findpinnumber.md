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
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523876"
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
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




