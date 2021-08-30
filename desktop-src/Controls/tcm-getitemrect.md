---
title: Message TCM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1a8a018cf63247831e07d0b4f1a64dd1469f96dd679409480e097712bb027d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060949"
---
# <a name="tcm_getitemrect-message"></a>\_Message GETITEMRECT TCM

Récupère le rectangle englobant d’un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’onglet.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant de l’onglet, dans les coordonnées de la fenêtre d’affichage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

