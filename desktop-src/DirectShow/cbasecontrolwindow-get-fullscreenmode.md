---
description: La \_ méthode obtenir FullScreenMode récupère le mode plein écran actuel.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Méthode CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923943"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>Méthode CBaseControlWindow. obten \_ FullScreenMode

La `get_FullScreenMode` méthode récupère le mode plein écran actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Pointeur vers le mode plein écran actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre retourne E \_ NOTIMPL par défaut. Cela informe le serveur de distribution de plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) que ce convertisseur n’implémente pas un convertisseur plein écran.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




