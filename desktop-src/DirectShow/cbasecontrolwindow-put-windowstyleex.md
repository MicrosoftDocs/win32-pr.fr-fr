---
description: La \_ méthode put WindowStyleEx définit les styles de fenêtre étendus.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Méthode CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537906"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>CBaseControlWindow. put \_ WindowStyleEx, méthode

La `put_WindowStyleEx` méthode définit les styles de fenêtre étendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*WindowStyleEx* \[ dans\]
</dt> <dd>

Valeur qui spécifie le style de la fenêtre de contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur.

## <a name="remarks"></a>Notes

Cette méthode utilise des styles de fenêtre étendus. Pour obtenir la liste complète des styles de fenêtre étendus, consultez la fonction Microsoft Win32 **CreateWindowEx** . Pour modifier le style de la fenêtre, récupérez le style de la fenêtre active, puis ajoutez ou supprimez les champs de bits nécessaires.

N’utilisez pas les styles de fenêtre suivants, car ils ne sont pas validés.

-   WS \_ désactivé
-   \_HSCROLL WS
-   \_sous forme WS
-   \_optimisation WS
-   WS \_ réduire
-   \_VSCROLL WS

À quelques exceptions près (notées ici), les indicateurs acceptables sont les mêmes que ceux autorisés par la fonction **CreateWindow** Win32.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




