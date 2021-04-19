---
description: La méthode DoSetWindowForeground amène la fenêtre au premier plan.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Méthode CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532537"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>Méthode CBaseWindow. DoSetWindowForeground

La `DoSetWindowForeground` méthode amène la fenêtre au premier plan.

## <a name="syntax"></a>Syntaxe


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bFocus* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut attribuer le focus à la fenêtre. Si la valeur est **true**, la fenêtre obtient le focus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




