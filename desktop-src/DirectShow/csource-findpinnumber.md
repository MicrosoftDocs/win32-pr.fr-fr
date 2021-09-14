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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010041"
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

## <a name="return-value"></a>Valeur de retour

Retourne le numéro de code confidentiel, ou 1 si le code PIN est introuvable sur ce filtre. Le premier code PIN est numéroté à zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




