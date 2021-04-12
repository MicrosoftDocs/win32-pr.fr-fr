---
title: Message LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtient les coordonnées d’un pied de page pour un élément spécifié dans un contrôle de vue liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterItemRect.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200540"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Message GETFOOTERITEMRECT LVM

Obtient les coordonnées d’un pied de page pour un élément spécifié dans un contrôle de vue liste. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de l’élément dans le contrôle List-View.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées. L’application appelante est chargée d’allouer cette structure. Les coordonnées reçues sont exprimées en tant que coordonnées clientes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

