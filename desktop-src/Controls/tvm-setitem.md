---
title: Message TVM_SETITEM (commctrl. h)
description: Le \_ message TVM SETITEM définit une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetItem TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9521bc67766dbb503fc205e966d6ce72e674a4050b6c0d237c885dcb4a8f4b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913939"
---
# <a name="tvm_setitem-message"></a>TVM \_ SETITEM message

Le message **TVM \_ SETITEM** définit une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient les nouveaux attributs d’élément. Avec la [version 4,71](common-control-versions.md) et les versions ultérieures, vous pouvez utiliser une structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) à la place.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifie l’élément et le membre **Mask** spécifie les attributs à définir.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) et **TVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





