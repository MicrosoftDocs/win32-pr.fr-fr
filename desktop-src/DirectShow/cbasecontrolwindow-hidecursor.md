---
description: La méthode HideCursor masque ou affiche le curseur.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Méthode CBaseControlWindow. HideCursor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6421a650471d0954031433db3814e8453cbc82586c7f37608ae947e7301c6969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158380"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>Méthode CBaseControlWindow. HideCursor

La `HideCursor` méthode masque ou affiche le curseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HideCursor* 
</dt> <dd>

Valeur spécifiant s’il faut afficher le curseur. Définissez sur OATRUE pour masquer le curseur, ou OAFALSE pour afficher le curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




