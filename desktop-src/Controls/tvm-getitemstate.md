---
title: Message TVM_GETITEMSTATE (commctrl. h)
description: Récupère tout ou partie des attributs d’état d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemState TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033040"
---
# <a name="tvm_getitemstate-message"></a>TVM \_ GETITEMSTATE message

Récupère tout ou partie des attributs d’état d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemState TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de l’élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Masque utilisé pour spécifier les États à interroger. Elle est équivalente au membre **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **uint** avec les bits d’État appropriés ayant la valeur **true**. Seuls les bits qui sont spécifiés par *lParam* et qui ont la **valeur true** seront définis. Cette valeur est équivalente au membre d' **État** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





