---
description: Se produit lorsque l’utilisateur déplace la souris alors que la souris se trouve sur le contrôle InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: InkEdit. MouseMove, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534599"
---
# <a name="inkeditmousemove-event"></a>InkEdit. MouseMove, événement

Se produit lorsque l’utilisateur déplace la souris alors que la souris se trouve sur le contrôle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Button* 
</dt> <dd>

Membre de l’énumération [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) qui indique les boutons de la souris qui sont enfoncés.



| Valeur                                                                                                                                                            | Signification                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**Non \_ BOUTON**</dt> </dl>             | Par défaut. Aucun bouton de la souris n'a été enfoncé. <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>À **gauche \_ BOUTON**</dt> </dl>       | Le bouton gauche de la souris a été enfoncé. <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>À **droite \_ BOUTON**</dt> </dl>    | Le bouton droit de la souris a été enfoncé. <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**Au milieu \_ BOUTON**</dt> </dl> | Le bouton central de la souris a été enfoncé. <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) qui indique quelles touches de modification sont enfoncées au moment de l’événement.



| Valeur                                                                                                                                                                                     | Signification                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Spécifie que la touche Maj a été utilisée comme modificateur. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Contrôle**</dt> </dl> | Spécifie que la touche CTRL a été utilisée comme modificateur. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Spécifie que la touche ALT a été utilisée comme modificateur. <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

Coordonnée x actuelle, en pixels, du pointeur de la souris.

</dd> <dt>

*yMouse* 
</dt> <dd>

Coordonnée y actuelle, en pixels, du pointeur de la souris.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si un bouton de la souris est enfoncé alors que le pointeur est sur un contrôle [InkEdit](inkedit-control-reference.md) , ce contrôle capture la souris et reçoit tous les événements de la souris jusqu’au dernier événement [**MouseUp**](inkedit-mouseup.md) , y compris celui-ci. Cela implique que les coordonnées du pointeur de la souris (x, y) retournées par un événement de souris ne se trouvent pas toujours dans la zone interne de l’objet qui les reçoit.

Si les boutons de la souris sont appuyés successivement, l’objet qui capture la souris après la première pression reçoit tous les événements de la souris jusqu’à ce que tous les boutons soient libérés.

L’événement **MouseMove** est généré continuellement lorsque le pointeur de la souris se déplace entre les objets. À moins qu’un autre objet n’ait capturé la souris, un contrôle [InkEdit](inkedit-control-reference.md) reconnaît un événement **MouseMove** lorsque la position de la souris se trouve dans ses limites.

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeMouseMove.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Énumération InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Énumération InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Événement MouseDown, \[ contrôle InkEdit\]**](inkedit-mousedown.md)
</dt> <dt>

[**Contrôle InkEdit de l’événement MouseUp \[\]**](inkedit-mouseup.md)
</dt> </dl>

 

