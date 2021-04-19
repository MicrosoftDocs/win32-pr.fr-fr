---
description: Publié dans la fenêtre qui a le focus lorsque l’utilisateur choisit une nouvelle langue d’entrée, soit avec la touche de raccourci (spécifiée dans l’application du panneau de configuration du clavier), soit à partir de l’indicateur de la barre des tâches système.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Message WM_INPUTLANGCHANGEREQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529170"
---
# <a name="wm_inputlangchangerequest-message"></a>\_Message WM INPUTLANGCHANGEREQUEST

Publié dans la fenêtre qui a le focus lorsque l’utilisateur choisit une nouvelle langue d’entrée, soit avec la touche de raccourci (spécifiée dans l’application du panneau de configuration du clavier), soit à partir de l’indicateur de la barre des tâches système. Une application peut accepter la modification en transmettant le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou refuser la modification (et l’empêcher d’avoir lieu) en retournant immédiatement.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouveaux paramètres régionaux d’entrée. Ce paramètre peut être une combinaison des indicateurs suivants.



| Valeur                                                                                                                                                                                                                                                            | Signification                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> inversé </dl>       | Une touche d’accès rapide a été utilisée pour choisir les paramètres régionaux d’entrée précédents dans la liste des paramètres régionaux d’entrée installés. Cet indicateur ne peut pas être utilisé avec l' \_ indicateur INPUTLANGCHANGE Forward.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ TRANSFÉRER**</dt> <dt>0x0002</dt> </dl>          | Une touche d’accès rapide a été utilisée pour choisir les paramètres régionaux d’entrée suivants dans la liste des paramètres régionaux d’entrée installés. Cet indicateur ne peut pas être utilisé avec l' \_ indicateur INPUTLANGCHANGE Backward.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt> </dl> | La nouvelle disposition de clavier de paramètres régionaux d’entrée peut être utilisée avec le jeu de caractères système.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de paramètres régionaux d’entrée. Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Ce message est publié, non envoyé, à l’application. la valeur de retour est donc ignorée. Pour accepter la modification, l’application doit transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Pour refuser la modification, l’application doit retourner zéro sans appeler **DefWindowProc**.

## <a name="remarks"></a>Notes

Lorsque la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) reçoit le message **WM \_ INPUTLANGCHANGEREQUEST** , elle active les nouveaux paramètres régionaux d’entrée et avertit l’application de la modification en envoyant le message [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) .

L’indicateur de langue n’est présent dans la barre des tâches que si vous avez installé plusieurs dispositions de clavier et si vous avez activé l’indicateur à l’aide de l’application du panneau de configuration du clavier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_INPUTLANGCHANGE WM**](wm-inputlangchange.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
