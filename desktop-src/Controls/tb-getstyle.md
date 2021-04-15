---
title: Message TB_GETSTYLE (commctrl. h)
description: Récupère les styles en cours d’utilisation pour un contrôle ToolBar.
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- TB_GETSTYLE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466322"
---
# <a name="tb_getstyle-message"></a>TO \_ GETSTYLE message

Récupère les styles en cours d’utilisation pour un contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui est une combinaison de [styles de contrôle de barre d’outils](toolbar-control-and-button-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





