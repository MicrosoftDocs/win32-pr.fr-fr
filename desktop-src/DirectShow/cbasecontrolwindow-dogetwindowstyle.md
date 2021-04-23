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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909817"
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



| Étiquette | Valeur |
|--------------|--------------------------------------|
| \_style GWL   | Récupérer les styles de fenêtre.          |
| GWL \_ EXstyle | Récupérer les styles de fenêtre étendus. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

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

 

 




