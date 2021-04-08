---
title: Message HDM_GETBITMAPMARGIN (commctrl. h)
description: Obtient la largeur de la marge de bitmap pour un contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetBitmapMargin.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942168"
---
# <a name="hdm_getbitmapmargin-message"></a>\_Message HDM GETBITMAPMARGIN

Obtient la largeur de la marge de bitmap pour un contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur, en pixels, de la marge de la bitmap. Si la marge de bitmap n’a pas été précédemment spécifiée, la valeur par défaut de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)
</dt> </dl>

 

