---
title: Message TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’arborescence pour définir des styles étendus. Envoyez ce message ou utilisez la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508694"
---
# <a name="tvm_setextendedstyle-message"></a>TVM \_ SETEXTENDEDSTYLE message

Informe le contrôle d’arborescence pour définir des styles étendus. Envoyez ce message ou utilisez la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Masque utilisé pour sélectionner les styles à définir.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur qui indique le style étendu. Pour plus d’informations sur les styles, consultez [styles étendus de contrôle d’arborescence](tree-view-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les styles étendus pour un contrôle d’arborescence n’ont rien à voir avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

