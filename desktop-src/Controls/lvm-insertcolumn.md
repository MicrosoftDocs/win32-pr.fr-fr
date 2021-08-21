---
title: Message LVM_INSERTCOLUMN (commctrl. h)
description: Insère une nouvelle colonne dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de ListView \_ InsertColumn.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019237"
---
# <a name="lvm_insertcolumn-message"></a>\_Message LVM INSERTCOLUMN

Insère une nouvelle colonne dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de la nouvelle colonne.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) qui contient les attributs de la nouvelle colonne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de la nouvelle colonne en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Remarques

Les colonnes sont visibles uniquement dans la vue rapport (détails).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





