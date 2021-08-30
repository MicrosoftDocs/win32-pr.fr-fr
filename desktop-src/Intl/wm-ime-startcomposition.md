---
description: Envoyé juste avant que l’IME génère la chaîne de composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Message WM_IME_STARTCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c45e429277fc2621956646f2f4d5c1162a5ad516b90fd2d4d1e60ffe01e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086479"
---
# <a name="wm_ime_startcomposition-message"></a>\_ \_ Message STARTCOMPOSITION de l’IME WM

Envoyé juste avant que l’IME génère la chaîne de composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

<dl></dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Ce message est une notification à une fenêtre IME permettant d’ouvrir sa fenêtre de composition. Une application doit traiter ce message si elle affiche lui-même des caractères de composition.

Si une application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite le message en le passant à la fenêtre IME par défaut.

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
</dt> </dl>

 

 
