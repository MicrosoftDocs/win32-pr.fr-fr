---
title: Message TB_GETSTYLE (commctrl. h)
description: Récupère les styles en cours d’utilisation pour un contrôle ToolBar.
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- TB_GETSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8de0addae729a4a8c641d21fd1771137d8c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116705"
---
# <a name="tb_getstyle-message"></a>TO \_ GETSTYLE message

Récupère les styles en cours d’utilisation pour un contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **DWORD** qui est une combinaison de [styles de contrôle de barre d’outils](toolbar-control-and-button-styles.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





