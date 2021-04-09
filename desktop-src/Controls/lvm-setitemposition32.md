---
title: Message LVM_SETITEMPOSITION32 (commctrl. h)
description: Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032918"
---
# <a name="lvm_setitemposition32-message"></a>\_Message SETITEMPOSITION32 LVM

Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône). Ce message diffère du message [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) en ce qu’il utilise des coordonnées 32 bits. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste pour lequel définir la position.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient la nouvelle position de l’élément, en coordonnées de vue de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

