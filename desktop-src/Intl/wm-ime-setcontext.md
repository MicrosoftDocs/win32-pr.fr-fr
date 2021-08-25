---
description: Envoyé à une application lorsqu’une fenêtre est activée. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Message WM_IME_SETCONTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fb3e65b47b5d62b1d37ffaee4dfc5927d76485d0c3e5de02662da64215e43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829249"
---
# <a name="wm_ime_setcontext-message"></a>Message de l' \_ IME SETCONTEXT du WM \_

Envoyé à une application lorsqu’une fenêtre est activée. Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

**True** si la fenêtre est active, et **false** dans le cas contraire.

</dd> <dt>

*lParam* 
</dt> <dd>

les options d’affichage ; Ce paramètre peut avoir une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                   | Signification                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | Affiche la fenêtre de composition par le biais de la fenêtre de l’interface utilisateur.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | Affichez la fenêtre Guide par le biais de la fenêtre de l’interface utilisateur.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | Affiche la fenêtre de l’interface utilisateur du clavier conditionnel.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt> </dl>       | Affiche la fenêtre candidate de l’index 0 par la fenêtre de l’interface utilisateur.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Affiche la fenêtre candidate de l’index 1 par la fenêtre de l’interface utilisateur.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Affiche la fenêtre candidate de l’index 2 par la fenêtre de l’interface utilisateur.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Affiche la fenêtre candidate de l’index 3 par la fenêtre de l’interface utilisateur.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur retournée par [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Remarques

Si l’application a créé une fenêtre IME, elle doit appeler [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Dans le cas contraire, il doit transmettre ce message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Si l’application dessine la fenêtre de composition, la fenêtre IME par défaut n’a pas besoin d’afficher sa fenêtre de composition. Dans ce cas, l’application doit effacer la **valeur ISC \_ SHOWUICOMPOSITIONWINDOW** du paramètre *lParam* avant de transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Pour afficher une certaine fenêtre de l’interface utilisateur, une application doit supprimer la valeur correspondante afin que l’IME ne l’affiche pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                                                      |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h);</dt> <dt>Imm. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
