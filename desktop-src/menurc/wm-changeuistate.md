---
title: Message WM_CHANGEUISTATE (winuser. h)
description: Une application envoie le \_ message WM CHANGEUISTATE pour indiquer que l’état de l’interface utilisateur doit être modifié.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3849f9a5d2ccd0cec1bcaba4280e125ea01a669c8535c2dc520ebb98c3a3fcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869709"
---
# <a name="wm_changeuistate-message"></a>\_Message WM CHANGEUISTATE

Une application envoie le message **WM \_ CHANGEUISTATE** pour indiquer que l’état de l’interface utilisateur doit être modifié.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie l’action à entreprendre. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                   | Signification                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Interfaces utilisateur \_ EFFACER**</dt> <dt>2</dt> </dl>                | Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être effacés.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Interfaces utilisateur \_ INITIALiser**</dt> <dt>3</dt> </dl> | Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être modifiés en fonction du dernier événement d’entrée. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Interfaces utilisateur \_ DÉFINIR**</dt> <dt>1</dt> </dl>                      | Les indicateurs d’état d’interface utilisateur spécifiés par le mot de poids fort doivent être définis.<br/>                                                                      |



 

Le mot de poids fort spécifie les éléments d’état d’interface utilisateur qui sont affectés ou le style du contrôle. Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                     | Signification                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_**</dt> <dt>0x4</dt> actif </dl>          | Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt> </dl> | Les accélérateurs clavier sont masqués.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Les indicateurs de focus sont masqués.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à 0.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une fenêtre doit envoyer ce message à lui-même ou à son parent lorsqu’il doit modifier les éléments d’état de l’interface utilisateur de toutes les fenêtres dans la même hiérarchie. La procédure de fenêtre doit laisser [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traiter ce message afin que l’ensemble de l’arborescence de la fenêtre ait un état d’interface utilisateur cohérent. Lorsque la fenêtre de niveau supérieur reçoit le message **WM \_ CHANGEUISTATE** , elle envoie un message [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) avec les mêmes paramètres à toutes les fenêtres enfants. Lorsque le système traite le message **WM \_ UPDATEUISTATE** , il effectue la modification dans l’état de l’interface utilisateur.

Si le mot de poids faible de *wParam* est \_ Initialize UIS, le système envoie le message [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) avec un état d’interface utilisateur basé sur le dernier événement d’entrée. Par exemple, si la dernière entrée provient de la souris, le système masque les indications de clavier. Et, si la dernière entrée provient du clavier, le système affiche les indications de clavier. Si l’État qui résulte du traitement de **WM \_ CHANGEUISTATE** est le même que celui de l’ancien, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) n’envoie pas ce message.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_QUERYUISTATE WM**](wm-queryuistate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

