---
title: Message LVM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant pour l’intégralité ou une partie d’un élément dans l’affichage actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemRect.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999814"
---
# <a name="lvm_getitemrect-message"></a>\_Message GETITEMRECT LVM

Récupère le rectangle englobant pour l’intégralité ou une partie d’un élément dans l’affichage actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant. Lorsque le message est envoyé, le membre de **gauche** de cette structure est utilisé pour spécifier la partie de l’élément de vue de liste à partir de laquelle récupérer le rectangle englobant. Elle doit être définie sur l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**\_limites LVIR**</dt> </dl>                   | Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**\_icône LVIR**</dt> </dl>                         | Retourne le rectangle englobant de l’icône ou de la petite icône.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_étiquette LVIR**</dt> </dl>                      | Retourne le rectangle englobant du texte de l’élément.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | Retourne l’Union des rectangles de l’icône LVIR et de l' \_ \_ étiquette LVIR, mais exclut les colonnes de la vue rapport.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

