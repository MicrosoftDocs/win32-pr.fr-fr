---
title: Message TVM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip enfant utilisé par un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetToolTips TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464762"
---
# <a name="tvm_gettooltips-message"></a>TVM \_ GETTOOLTIPS message

Récupère le handle du contrôle ToolTip enfant utilisé par un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetToolTips TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip enfant, ou **null** si le contrôle n’utilise pas d’info-bulles.

## <a name="remarks"></a>Notes

En cas de création, les contrôles d’arborescence créent automatiquement un contrôle ToolTip enfant. Pour faire en sorte qu’un contrôle d’arborescence n’utilise pas les info-bulles, créez le contrôle avec le style [**TV \_ noInfos**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETTOOLTIPS**](tvm-settooltips.md)
</dt> </dl>

 

 





