---
title: Message LVM_GETBKCOLOR (commctrl. h)
description: Obtient la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetBkColor.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- LVM_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464286"
---
# <a name="lvm_getbkcolor-message"></a>\_Message GETBKCOLOR LVM

Obtient la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur d’arrière-plan du contrôle List-View.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





