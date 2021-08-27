---
title: Message LVM_DELETEALLITEMS (commctrl. h)
description: Supprime tous les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView DeleteAllItems.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958408"
---
# <a name="lvm_deleteallitems-message"></a>\_Message DELETEALLITEMS LVM

Supprime tous les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Lorsqu’un contrôle List-View reçoit le **message \_ DELETEALLITEMS LVM** , il envoie le code de notification [**\_ DELETEALLITEMS LVN**](lvn-deleteallitems.md) à sa fenêtre parente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





