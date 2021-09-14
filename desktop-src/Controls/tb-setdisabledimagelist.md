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
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116578"
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

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons désactivés, ou **null** si aucune liste d’images n’a été définie précédemment.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





