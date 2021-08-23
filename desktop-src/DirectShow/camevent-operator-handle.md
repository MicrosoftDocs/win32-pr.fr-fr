---
description: Récupère le handle d’événement. Cet opérateur n’est pas pris en charge en tant que L-value.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Méthode de HANDLE CAMEvent. Operator (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afc3bcc1044d3d14b7ebf77ce12027fb3b772185f62b917fce7b74fbb3fa7e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689329"
---
# <a name="cameventoperator-handle-method"></a>CAMEvent. Operator, méthode de HANDLE

Récupère le handle d’événement. Cet opérateur n’est pas pris en charge en tant que L-value.

## <a name="syntax"></a>Syntaxe


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CAMEvent :: m \_ hEvent**](camevent-m-hevent.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMEvent, classe**](camevent.md)
</dt> </dl>

 

 




