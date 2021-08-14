---
description: Se produit lorsque l’utilisateur relâche une touche alors que le contrôle InkEdit a le focus.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Événement InkEdit. KeyUp (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ac908202a22fc1f564c3f21da4cc3cce2e79e2f093ec93b65ff56066f94510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220754"
---
# <a name="inkeditkeyup-event"></a>InkEdit. KeyUp, événement

Se produit lorsque l’utilisateur relâche une touche alors que le contrôle [InkEdit](inkedit-control-reference.md) a le focus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*A-la* 
</dt> <dd>

Code de la touche virtuelle de la touche enfoncée par l’utilisateur.

</dd> <dt>

*ShiftKey* 
</dt> <dd>

Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) qui indique quelles touches de modification sont enfoncées au moment de l’événement.



| Valeur                                                                                                                                                                                     | Signification                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | Spécifie que la touche Maj a été utilisée comme modificateur. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Contrôle**</dt> </dl> | Spécifie que la touche CTRL a été utilisée comme modificateur. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Spécifie que la touche ALT a été utilisée comme modificateur. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyUp.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Énumération InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyOut, événement \[ InkEdit, contrôle\]**](inkedit-keydown.md)
</dt> <dt>

[**Événement KeyPress \[ InkEdit, contrôle\]**](inkedit-keypress.md)
</dt> </dl>

 

