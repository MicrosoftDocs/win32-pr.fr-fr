---
title: Message LVM_SETITEMPOSITION (commctrl. h)
description: Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône). Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemPosition.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION les contrôles de message Windows
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
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843666"
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

## <a name="remarks"></a>Notes

Si le contrôle de vue de liste a le style de [**\_ réorganisation LVS**](list-view-window-styles.md) , les éléments du contrôle d’affichage de liste sont disposés après la définition de la position de l’élément.

Sur Windows Vista, l’envoi de ce message à un contrôle List-View avec le style [**\_ AutoArrange LVS**](list-view-window-styles.md) ne fait rien, et la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

