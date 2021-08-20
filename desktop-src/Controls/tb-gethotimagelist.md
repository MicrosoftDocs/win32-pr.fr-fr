---
title: Message TB_GETHOTIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons actifs.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168512"
---
# <a name="tb_gethotimagelist-message"></a>TO \_ GETHOTIMAGELIST message

Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons actifs.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images que le contrôle utilise pour afficher les boutons actifs, ou **null** si aucune liste d’images réactives n’est définie.

## <a name="remarks"></a>Remarques

Un bouton est actif lorsque le curseur se trouve sur celui-ci. Les contrôles ToolBar doivent avoir le style de [**\_ liste**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plat**](toolbar-control-and-button-styles.md) ou TBSTYLE pour avoir des éléments chauds.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





