---
title: Message WM_UPDATEUISTATE (winuser. h)
description: Une application envoie le \_ message WM UPDATEUISTATE pour modifier l’état de l’interface utilisateur pour la fenêtre spécifiée et toutes ses fenêtres enfants.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106453"
---
# <a name="wm_updateuistate-message"></a>\_Message WM UPDATEUISTATE

Une application envoie le message **WM \_ UPDATEUISTATE** pour modifier l’état de l’interface utilisateur pour la fenêtre spécifiée et toutes ses fenêtres enfants.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie l’action à exécuter. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                   | Signification                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Interfaces utilisateur \_ EFFACER**</dt> <dt>2</dt> </dl>                | L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être masqué.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Interfaces utilisateur \_ INITIALiser**</dt> <dt>3</dt> </dl> | L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être modifié en fonction du dernier événement d’entrée. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Interfaces utilisateur \_ DÉFINIR**</dt> <dt>1</dt> </dl>                      | L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être visible.<br/>                                                                  |



 

Le mot de poids fort spécifie les éléments d’état d’interface utilisateur qui sont affectés ou le style du contrôle. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                     | Signification                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_**</dt> <dt>0x4</dt> actif </dl>          | Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt> </dl> | Accélérateurs clavier.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Indicateurs de focus.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Une fenêtre doit envoyer ce message pour modifier l’état de l’interface utilisateur de toutes ses fenêtres enfants. Contrairement au message [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , qui est une notification, lorsque [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite le message **WM \_ UPDATEUISTATE** , il modifie l’état de l’interface utilisateur et propage les modifications à toutes les fenêtres enfants.

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) met à jour l’état de l’interface utilisateur en fonction de la valeur *wParam* . Si l’état de l’interface utilisateur est modifié, la fonction envoie le message à toutes les fenêtres enfants immédiats. **DefWindowProc** envoie également ce message lorsqu’il reçoit un message [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) notifiant au système qu’une fenêtre enfant a l’intention de modifier l’état de l’interface utilisateur.

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

[**\_CHANGEUISTATE WM**](wm-changeuistate.md)
</dt> <dt>

[**\_QUERYUISTATE WM**](wm-queryuistate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

