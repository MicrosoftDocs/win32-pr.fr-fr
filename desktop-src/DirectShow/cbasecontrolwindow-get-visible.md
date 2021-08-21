---
description: La \_ méthode visible récupère la visibilité de la fenêtre active.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Méthode CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef75aaf396e8677e9c470239d5dfca747729b534b67f8fef53a065280175f017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017377"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow. obtient la \_ méthode visible

La `get_Visible` méthode récupère la visibilité de la fenêtre active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVisible* 
</dt> <dd>

Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre retourne 1 si la fenêtre a le \_ style WS visible ; sinon, 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




