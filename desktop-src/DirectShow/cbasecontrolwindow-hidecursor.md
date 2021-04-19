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
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536039"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




