---
title: Message TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’arborescence pour définir des styles étendus. Envoyez ce message ou utilisez la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE les contrôles de Windows de message
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
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750959"
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

## <a name="remarks"></a>Remarques

Les styles étendus pour un contrôle d’arborescence n’ont rien à voir avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

