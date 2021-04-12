---
title: Message WM_ENTERIDLE (winuser. h)
description: Envoyé à la fenêtre propriétaire d’un menu ou d’une boîte de dialogue modale qui passe à l’état inactif. Un menu ou une boîte de dialogue modale passe à l’état inactif quand aucun message n’est en attente dans sa file d’attente après avoir traité un ou plusieurs messages précédents.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Boîtes de dialogue de WM_ENTERIDLE message
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385036"
---
# <a name="wm_enteridle-message"></a>\_Message WM ENTERIDLE

Envoyé à la fenêtre propriétaire d’un menu ou d’une boîte de dialogue modale qui passe à l’état inactif. Un menu ou une boîte de dialogue modale passe à l’état inactif quand aucun message n’est en attente dans sa file d’attente après avoir traité un ou plusieurs messages précédents.


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                   | Signification                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt> </dl> | Le système est inactif, car une boîte de dialogue s’affiche.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENU**</dt> <dt>2</dt> </dl>                | Le système est inactif, car un menu est affiché.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la boîte de dialogue (si *wParam* est **MSGF \_ DialogBox**) ou fenêtre contenant le menu affiché (si *wParam* est **le \_ menu MSGF**).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Vous pouvez supprimer le message **WM \_ ENTERIDLE** pour une boîte de dialogue en créant la boîte de dialogue avec le style **DS \_ NOIDLEMSG** .

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

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

