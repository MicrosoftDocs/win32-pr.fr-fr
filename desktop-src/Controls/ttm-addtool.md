---
title: Message TTM_ADDTOOL (commctrl. h)
description: Inscrit un outil avec un contrôle ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb66c43033e54ce51b396ff5bb11efe3b2a99e8eb2578a2e9fe4d4bc4487ccf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769539"
---
# <a name="ttm_addtool-message"></a>\_Message atténuation ADDTOOL

Inscrit un outil avec un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contenant les informations dont le contrôle ToolTip a besoin pour afficher le texte de l’outil. Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ ADDTOOLW** (Unicode) et **atténuation \_ ADDTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ATTÉNUATION \_ DELTOOL**](ttm-deltool.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos des contrôles ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





