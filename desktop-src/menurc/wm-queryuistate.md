---
title: Message WM_QUERYUISTATE (winuser. h)
description: Une application envoie le \_ message WM QUERYUISTATE pour récupérer l’état de l’interface utilisateur d’une fenêtre.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512212"
---
# <a name="wm_queryuistate-message"></a>\_Message WM QUERYUISTATE

Une application envoie le message **WM \_ QUERYUISTATE** pour récupérer l’état de l’interface utilisateur d’une fenêtre.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **null** si les indicateurs de focus et les accélérateurs de clavier sont visibles. Dans le cas contraire, la valeur de retour peut être une ou plusieurs des valeurs suivantes.



| Code/valeur de retour                                                                                                                                       | Description                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_**</dt> <dt>0x4</dt> actif </dl>    | Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.<br/> |
| <dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt> </dl> | Les accélérateurs clavier sont masqués.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Les indicateurs de focus sont masqués.<br/>                                     |



 

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

[**\_CHANGEUISTATE WM**](wm-changeuistate.md)
</dt> <dt>

[**\_UPDATEUISTATE WM**](wm-updateuistate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

 





