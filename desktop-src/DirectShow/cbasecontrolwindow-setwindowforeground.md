---
description: La méthode SetWindowForeground déplace la fenêtre vidéo au premier plan et, éventuellement, lui donne le focus.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Méthode CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87a6768c8864de45d50dc630773b756dfad43759adbf4b09ed8070febd37f4d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635469"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>Méthode CBaseControlWindow. SetWindowForeground

La `SetWindowForeground` méthode déplace la fenêtre vidéo au premier plan et, éventuellement, lui donne le focus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Priorité* 
</dt> <dd>

Valeur qui spécifie si la fenêtre vidéo obtient le focus. La valeur 1 donne le focus de la fenêtre et 0 ne le fait pas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                           | Description                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | S_OK<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Le focus n’est pas égal à 1 ou 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le filtre actuel n’est pas connecté à un graphique de filtre complet.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




