---
description: Envoyé à une application lorsque l’IME termine la composition. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Message WM_IME_ENDCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9e19bcf1834d4f9e721efb2a2be53ca20268c7be42109975a7dea52e75d214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560399"
---
# <a name="wm_ime_endcomposition-message"></a>\_ \_ Message ENDCOMPOSITION de l’IME WM

Envoyé à une application lorsque l’IME termine la composition. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
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

Une application doit traiter ce message si elle affiche lui-même des caractères de composition.

Si l’application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en le passant à la fenêtre IME par défaut.

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

 

 
