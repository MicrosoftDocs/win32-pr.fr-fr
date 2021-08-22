---
description: Envoyé à une application par l’IME pour notifier l’application d’une pression de touche et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Message WM_IME_KEYDOWN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535309"
---
# <a name="wm_ime_keydown-message"></a>\_Message de \_ keyversion de l’IME WM

Envoyé à une application par l’IME pour notifier l’application d’une pression de touche et conserver l’ordre des messages. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
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

Le tableau suivant indique le nombre de répétitions, l’analyse du code, l’indicateur de clé étendu, le code de contexte, l’indicateur d’état de la clé précédente et l’indicateur d’état de transition.



| bit   | Signification                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions.                                                               |
| 16-23 | Analyser le code.                                                                  |
| 24    | Clé étendue. Cette valeur est 1 s’il s’agit d’une clé étendue. Sinon, la valeur est 0. |
| 25-28 | Non utilisé.                                                                   |
| 29    | Code de contexte. Cette valeur est toujours 0.                                       |
| 30    | État de la clé précédente. Cette valeur est 1 si la touche est enfoncée ou 0 si elle est active.    |
| 31    | État de transition. Cette valeur est toujours 0.                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner 0 si elle traite ce message.

## <a name="remarks"></a>Remarques

Une application peut traiter ce message ou la passer à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour générer un message [**de \_ keyversion WM**](../inputdev/wm-keydown.md) correspondant.

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

 

 
