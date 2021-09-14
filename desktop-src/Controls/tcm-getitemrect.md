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
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116205"
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

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

