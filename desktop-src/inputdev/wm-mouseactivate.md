---
title: Message WM_MOUSEACTIVATE (winuser. h)
description: Envoyé lorsque le curseur se trouve dans une fenêtre inactive et que l’utilisateur appuie sur un bouton de la souris. La fenêtre parente reçoit ce message uniquement si la fenêtre enfant la passe à la fonction DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- WM_MOUSEACTIVATE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15116c36ac9efb3e764564fbe426f8763508fd63759e02bd4bb9160d5815fb11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451509"
---
# <a name="wm_mouseactivate-message"></a>\_Message WM MOUSEACTIVATE

Envoyé lorsque le curseur se trouve dans une fenêtre inactive et que l’utilisateur appuie sur un bouton de la souris. La fenêtre parente reçoit ce message uniquement si la fenêtre enfant la passe à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre parente de niveau supérieur de la fenêtre en cours d’activation.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) suite au traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) . Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.

Le mot de poids fort spécifie l’identificateur du message de souris généré quand l’utilisateur appuie sur un bouton de la souris. Le message de la souris est soit ignoré, soit publié dans la fenêtre, en fonction de la valeur de retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour spécifie si la fenêtre doit être activée et si l’identificateur du message de la souris doit être ignoré. Il doit s’agir de l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                          | Description                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**Ma \_ ACTIVER**</dt> <dt>1</dt> </dl>         | Active la fenêtre et n’ignore pas le message de la souris.<br/>         |
| <dl> <dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt> </dl>   | Active la fenêtre et ignore le message de la souris.<br/>                 |
| <dl> <dt>**Ma \_ Noactivate**</dt> <dt>3</dt> </dl>       | N’active pas la fenêtre et n’ignore pas le message de la souris.<br/> |
| <dl> <dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt> </dl> | N’active pas la fenêtre, mais ignore le message de la souris.<br/>         |



 

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) transmet le message à la fenêtre parente d’une fenêtre enfant avant tout traitement. La fenêtre parente détermine s’il faut activer la fenêtre enfant. Si elle active la fenêtre enfant, la fenêtre parente doit retourner **ma \_ noactivate** ou **ma \_ NOACTIVATEANDEAT** pour empêcher le système de traiter le message plus en détail.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_NCHITTEST WM**](wm-nchittest.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> </dl>

 

