---
title: Message LVM_HITTEST (commctrl. h)
description: Détermine l’élément de la vue de liste, le cas échéant, à une position spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958168"
---
# <a name="lvm_hittest-message"></a>Message LVM LVM \_

Détermine l’élément de la vue de liste, le cas échéant, à une position spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être égal à 0. **Windows Vista.** Doit avoir la valeur-1 si les membres **iGroup** et **iSubItem** de la structure *lParam* doivent être récupérés.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) qui contient la position à laquelle effectuer un test de positionnement et reçoit des informations sur les résultats du test de positionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément à la position spécifiée, le cas échéant, ou-1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





