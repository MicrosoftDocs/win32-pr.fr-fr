---
description: La méthode PossiblyEatMessage permet à une classe dérivée de transférer des messages à une autre fenêtre.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Méthode CBaseWindow. PossiblyEatMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016457"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Méthode CBaseWindow. PossiblyEatMessage

La `PossiblyEatMessage` méthode permet à une classe dérivée de transférer des messages à une autre fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uMsg* 
</dt> <dd>

Identificateur du message.

</dd> <dt>

*wParam* 
</dt> <dd>

Premier paramètre de message.

</dd> <dt>

*lParam* 
</dt> <dd>

Deuxième paramètre de message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le message a été transféré, ou **false** dans le cas contraire. La classe de base retourne **false**.

## <a name="remarks"></a>Remarques

Avant que la méthode [**CBaseWindow :: OnReceiveMessage**](cbasewindow-onreceivemessage.md) gère un message, elle appelle `PossiblyEatMessage` . Si `PossiblyEatMessage` retourne **true**, **OnReceiveMessage** ignore le message. Une classe dérivée peut être substituée `PossiblyEatMessage` afin de transférer des messages à une fenêtre propriétaire. Par exemple, la classe [**CBaseControlWindow**](cbasecontrolwindow.md) , qui dérive de **CBaseWindow**, transfère les messages de clavier et de souris.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




