---
title: Message HDM_GETITEMRECT (commctrl. h)
description: Obtient le rectangle englobant pour un élément donné dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetItemRect.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465886"
---
# <a name="hdm_getitemrect-message"></a>\_Message HDM GETITEMRECT

Obtient le rectangle englobant pour un élément donné dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de base zéro de l’élément de contrôle d’en-tête pour lequel récupérer le rectangle englobant.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/windows/win32/api/windef/ns-windef-rect) qui reçoit les informations de rectangle englobant. L’expéditeur du message est chargé d’allouer cette structure. Les coordonnées retournées dans la structure RECT sont exprimées par rapport au parent du contrôle header.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





