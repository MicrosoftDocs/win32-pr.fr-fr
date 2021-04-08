---
title: Message HDM_SETBITMAPMARGIN (commctrl. h)
description: Définit la largeur de la marge, spécifiée en pixels, d’une image bitmap dans un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetBitmapMargin.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844041"
---
# <a name="hdm_setbitmapmargin-message"></a>\_Message HDM SETBITMAPMARGIN

Définit la largeur de la marge, spécifiée en pixels, d’une image bitmap dans un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Largeur, spécifiée en pixels, de la marge qui entoure une bitmap dans un contrôle d’en-tête existant.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur de la marge de la bitmap, en pixels. Si la marge de bitmap n’a pas été précédemment spécifiée, la valeur par défaut de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

