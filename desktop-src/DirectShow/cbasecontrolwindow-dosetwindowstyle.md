---
description: La méthode DoSetWindowStyle modifie les styles de fenêtre par défaut ou étendus.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Méthode CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540353"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Méthode CBaseControlWindow. DoSetWindowStyle

La `DoSetWindowStyle` méthode modifie les styles de fenêtre par défaut ou étendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Style* 
</dt> <dd>

Styles de fenêtre appropriés.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valeur spécifiant les styles à définir. Doit prendre l'une des valeurs suivantes :



|              |                                      |
|--------------|--------------------------------------|
| \_style GWL   | Récupérer les styles de fenêtre.          |
| GWL \_ EXstyle | Récupérer les styles de fenêtre étendus. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre appelle la fonction Win32 **SetWindowLong** pour définir le style de la fenêtre, puis réaffiche la fenêtre dans la position actuelle. Cette fonction membre est appelée par les fonctions membres [**CBaseControlWindow ::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) et [**CBaseControlWindow ::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




