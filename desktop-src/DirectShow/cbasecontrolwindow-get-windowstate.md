---
description: La \_ méthode obtenir WindowState récupère l’état actuel de la fenêtre.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Méthode CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923907"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>CBaseControlWindow. obten, \_ méthode WindowState

La `get_WindowState` méthode récupère l’état actuel de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWindowState* 
</dt> <dd>

Pointeur vers l’état de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre retourne un sous-ensemble des paramètres de la fonction Microsoft Win32 **ShowWindow** . En particulier, elle retourne l' \_ affichage logiciel et le \_ masquage logiciel, selon la visibilité actuelle de la fenêtre. Il retourne également \_ les logiciels Minimize et \_ maximiser, selon que la fenêtre est une icône ou qu’elle est développée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




