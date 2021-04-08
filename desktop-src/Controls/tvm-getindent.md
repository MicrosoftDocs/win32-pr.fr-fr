---
title: Message TVM_GETINDENT (commctrl. h)
description: Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetIndent TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844250"
---
# <a name="tvm_getindent-message"></a>TVM \_ GETINDENT message

Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la mise en retrait.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





