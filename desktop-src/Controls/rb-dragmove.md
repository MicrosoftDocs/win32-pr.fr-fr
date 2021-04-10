---
title: Message RB_DRAGMOVE (commctrl. h)
description: Met à jour la position de glissement dans le contrôle rebar après un \_ message RB BEGINDRAG précédent.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942463"
---
# <a name="rb_dragmove-message"></a>\_Message DRAGMOVE RB

Met à jour la position de glissement dans le contrôle rebar après un message [**RB \_ BEGINDRAG**](rb-begindrag.md) précédent.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **DWORD** qui contient les nouvelles coordonnées de la souris. La coordonnée horizontale est contenue dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la coordonnée verticale est contenue dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si vous transmettez (DWORD)-1, le contrôle rebar utilise la position de la souris la dernière fois que le thread du contrôle a appelé [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ENDDRAG RB**](rb-enddrag.md)
</dt> </dl>

 

