---
description: La méthode DoGetWindowStyle récupère les styles de fenêtre normaux ou étendus actuels.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Méthode CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533070"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Méthode CBaseControlWindow. DoGetWindowStyle

La `DoGetWindowStyle` méthode récupère les styles de fenêtre standard actuels ou étendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStyle* 
</dt> <dd>

Pointeur vers une variable qui reçoit les informations de style.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valeur spécifiant les styles à récupérer. Doit prendre l'une des valeurs suivantes :



|              |                                      |
|--------------|--------------------------------------|
| \_style GWL   | Récupérer les styles de fenêtre.          |
| GWL \_ EXstyle | Récupérer les styles de fenêtre étendus. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre appelle la fonction Win32 **GetWindowLong** pour récupérer le style de fenêtre. Elle est appelée par les fonctions membres [**CBaseControlWindow :: obten \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) et [**CBaseControlWindow :: obten \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




