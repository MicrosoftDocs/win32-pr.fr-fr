---
title: Message TVM_SETTOOLTIPS (commctrl. h)
description: Définit le contrôle d’info-bulle enfant d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetToolTips TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115558"
---
# <a name="tvm_settooltips-message"></a>TVM \_ SETTOOLTIPS message

Définit le contrôle d’info-bulle enfant d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetToolTips TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle d’un contrôle ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle du contrôle ToolTip précédemment défini pour le contrôle Tree-View, ou **null** si les info-bulles n’ont pas été utilisées précédemment.

## <a name="remarks"></a>Notes

En cas de création, les contrôles d’arborescence créent automatiquement un contrôle ToolTip enfant. Pour empêcher l’affichage d’un contrôle d’arborescence à l’aide d’info-bulles, créez le contrôle avec le style [**TV \_ noInfos**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETTOOLTIPS**](tvm-gettooltips.md)
</dt> </dl>

 

 





