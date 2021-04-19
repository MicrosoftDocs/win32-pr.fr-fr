---
description: La \_ méthode put WindowStyle définit les styles de fenêtre standard.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Méthode CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541531"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow. put, \_ méthode WindowStyle

La `put_WindowStyle` méthode définit les styles de fenêtre standard.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Nouveaux styles de fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Soyez vigilant lorsque vous modifiez les styles de fenêtre. Dans la plupart des cas, une application doit récupérer le style actuel, puis ajouter ou supprimer les bits inappropriés. Cette procédure permet à différents styles de fenêtre internes utilisés par Windows de rester intacts.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




