---
title: Message LVM_SETCOLUMN (commctrl. h)
description: Définit les attributs d’une colonne de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetColumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942164"
---
# <a name="lvm_setcolumn-message"></a>\_Message SETCOLUMN LVM

Définit les attributs d’une colonne de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de la colonne.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) qui contient les nouveaux attributs de colonne. Le membre **Mask** spécifie les attributs de colonne à définir. Si le membre de **masque** spécifie la \_ valeur de texte LVCF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) et **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





