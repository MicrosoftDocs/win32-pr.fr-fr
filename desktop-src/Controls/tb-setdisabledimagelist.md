---
title: Message TB_SETDISABLEDIMAGELIST (commctrl. h)
description: Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST les contrôles de message Windows
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
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033093"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





