---
title: Message TVM_SETINDENT (commctrl. h)
description: Définit la largeur du retrait pour un contrôle d’arborescence et redessine le contrôle pour refléter la nouvelle largeur. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetIndent TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104179"
---
# <a name="tvm_setindent-message"></a>TVM \_ SETINDENT message

Définit la largeur du retrait pour un contrôle d’arborescence et redessine le contrôle pour refléter la nouvelle largeur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Largeur, en pixels, de la mise en retrait. Si ce paramètre est inférieur à la largeur minimale définie par le système, la nouvelle largeur est définie sur la valeur minimale définie par le système.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La valeur de mise en retrait minimale définie par le système est généralement de cinq pixels, mais elle n’est pas fixe. Pour récupérer la valeur exacte du retrait minimal sur un système particulier, envoyez un message de **TVM \_ SETINDENT** avec *wParam* défini à zéro. Envoyez ensuite un message [**TVM \_ GETINDENT**](tvm-getindent.md) pour récupérer la valeur de retrait minimale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





