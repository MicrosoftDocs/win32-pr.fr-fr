---
title: Message TVM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère le style étendu pour un contrôle Tree-View. Envoyez ce message explicitement ou à l’aide de la \_ macro GetExtendedStyle TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93eb22b3dfdbe05365d28a7c93bfa9df3619796f9b4ae9ec603c74da252c5a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834199"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>Message TVM_GETEXTENDEDSTYLE (commctrl. h)

Récupère le style étendu pour un contrôle Tree-View. Envoyez ce message explicitement ou à l’aide de la macro [**\_ GetExtendedStyle TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du style étendu. Pour plus d’informations sur les styles, consultez [styles étendus de contrôle d’arborescence](tree-view-control-window-extended-styles.md).

## <a name="remarks"></a>Remarques

Les styles étendus pour un contrôle d’arborescence n’ont rien à voir avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

