---
title: Message LVM_GETHOTCURSOR (commctrl. h)
description: Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743005"
---
# <a name="lvm_gethotcursor-message"></a>\_Message GETHOTCURSOR LVM

Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HCURSOR qui est le handle du curseur que le contrôle d’affichage de liste utilise lorsque la sélection active est activée.

## <a name="remarks"></a>Notes

Un contrôle List-View utilise le suivi réactif et la sélection au pointage lorsque le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





