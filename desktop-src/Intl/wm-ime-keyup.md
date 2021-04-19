---
description: Envoyé à une application par l’IME pour notifier l’application d’une version de clé et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Message WM_IME_KEYUP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515036"
---
# <a name="wm_ime_keyup-message"></a>\_Message de retouche de l’IME WM \_

Envoyé à une application par l’IME pour notifier l’application d’une version de clé et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
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

Code de clé virtuelle de la clé.

</dd> <dt>

*lParam* 
</dt> <dd>

Nombre de répétitions, code d’analyse, indicateur de clé étendue, code de contexte, indicateur d’état de clé précédent et indicateur d’état de transition, comme indiqué ci-dessous.



| bit   | Signification                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions. Cette valeur est toujours 1.                                       |
| 16-23 | Analyser le code.                                                                  |
| 24    | Clé étendue. Cette valeur est 1 s’il s’agit d’une clé étendue. Sinon, la valeur est 0. |
| 25-28 | Non utilisé.                                                                   |
| 29    | Code de contexte. Cette valeur est toujours 0.                                       |
| 30    | État de la clé précédente. Cette valeur est toujours 1.                                 |
| 31    | État de transition. Cette valeur est toujours 1.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner 0 si elle traite ce message.

## <a name="remarks"></a>Notes

Une application peut traiter ce message ou la passer à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour générer un message [**WM \_ KEYUP**](../inputdev/wm-keyup.md) correspondant.

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

 

 
