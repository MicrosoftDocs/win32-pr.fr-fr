---
description: Se produit lorsque l’utilisateur relâche une touche alors que le contrôle InkEdit a le focus.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Événement InkEdit. KeyUp (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530045"
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

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyUp.

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

[**Énumération InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyOut, événement \[ InkEdit, contrôle\]**](inkedit-keydown.md)
</dt> <dt>

[**Événement KeyPress \[ InkEdit, contrôle\]**](inkedit-keypress.md)
</dt> </dl>

 

