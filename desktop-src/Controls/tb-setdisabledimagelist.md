---
title: Message TB_SETDISABLEDIMAGELIST (commctrl. h)
description: Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9125c5e5ac742f4692fc5464cd51c89e111558c4d0004e08d7cef9c862d03cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167489"
---
# <a name="tb_setdisabledimagelist-message"></a>TO \_ SETDISABLEDIMAGELIST message

Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images qui sera définie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons désactivés, ou **null** si aucune liste d’images n’a été définie précédemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





