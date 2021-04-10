---
description: Envoyé à une application lorsque la fenêtre IME ne trouve aucun espace pour étendre la zone de la fenêtre de composition. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Message WM_IME_COMPOSITIONFULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210931"
---
# <a name="wm_ime_compositionfull-message"></a>\_ \_ Message COMPOSITIONFULL de l’IME WM

Envoyé à une application lorsque la fenêtre IME ne trouve aucun espace pour étendre la zone de la fenêtre de composition. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

<dl></dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

L’application doit utiliser la commande [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) pour spécifier la façon dont la fenêtre doit être affichée.

La fenêtre IME, au lieu de l’IME, envoie ce message de notification par la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> <dt>

[\_SETCOMPOSITIONWINDOW IMC](imc-setcompositionwindow.md)
</dt> </dl>

 

 
