---
title: Message LVM_SETHOTCURSOR (commctrl. h)
description: Définit la valeur HCURSOR utilisée par le contrôle List-View lorsque le pointeur se trouve sur un élément alors que la sélection active est activée.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3407c5d8b53483d3a639fc40959768b3fa8eea0e7b439ab8871d36346b7079d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077249"
---
# <a name="lvm_sethotcursor-message"></a>\_Message SETHOTCURSOR LVM

Définit la valeur HCURSOR utilisée par le contrôle List-View lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) . Pour vérifier si la surveillance à chaud est activée, appelez [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle du curseur à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HCURSOR qui est le curseur réactif précédent.

## <a name="remarks"></a>Remarques

Un contrôle List-View utilise le suivi réactif et la sélection au pointage lorsque le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

