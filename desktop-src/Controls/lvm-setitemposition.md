---
title: Message LVM_SETITEMPOSITION (commctrl. h)
description: Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône). Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemPosition.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111f961b668e13fa10fdfb00cdf430aba1bc9d0b1c0b04295e5777a46f5cb9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915249"
---
# <a name="lvm_setitemposition-message"></a>\_Message SETITEMPOSITION LVM

Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône). Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la nouvelle position x du coin supérieur gauche de l’élément, dans les coordonnées de la vue. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la nouvelle position y du coin supérieur gauche de l’élément, dans les coordonnées de la vue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si le contrôle de vue de liste a le style de [**\_ réorganisation LVS**](list-view-window-styles.md) , les éléments du contrôle d’affichage de liste sont disposés après la définition de la position de l’élément.

sur Windows Vista, l’envoi de ce message à un contrôle list-view avec le style [**\_ autoarrange LVS**](list-view-window-styles.md) ne fait rien, et la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

