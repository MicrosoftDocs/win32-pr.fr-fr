---
title: Message TB_SETHOTIMAGELIST (commctrl. h)
description: Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons actifs.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318849"
---
# <a name="tb_sethotimagelist-message"></a>TO \_ SETHOTIMAGELIST message

Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons actifs.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images qui sera définie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons actifs, ou **null** si aucune liste d’images n’a été définie précédemment.

## <a name="remarks"></a>Remarques

Un bouton est actif lorsque le curseur se trouve sur celui-ci. Les contrôles ToolBar doivent avoir le style de [**\_ liste**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plat**](toolbar-control-and-button-styles.md) ou TBSTYLE pour avoir des éléments chauds.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





