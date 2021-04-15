---
title: Message TBM_SETPOSNOTIFY (commctrl. h)
description: Définit la position logique actuelle du curseur dans un TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464771"
---
# <a name="tbm_setposnotify-message"></a>\_Message TBM SETPOSNOTIFY

Définit la position logique actuelle du curseur dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

wParam n’est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle position logique du curseur. Les positions logiques valides sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur. Si cette valeur est en dehors de la plage maximale et minimale du contrôle, la position est définie sur la valeur maximale ou minimale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’appel de **TBM \_ SETPOSNOTIFY** définit l’emplacement du curseur de la barre de défilement de la barre de défilement, comme [**TBM \_ SetPos**](tbm-setpos.md) , mais il fait également en sorte que le TrackBar informe son parent d’un déplacement via un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





