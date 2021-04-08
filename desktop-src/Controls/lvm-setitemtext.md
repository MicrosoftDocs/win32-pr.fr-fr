---
title: Message LVM_SETITEMTEXT (commctrl. h)
description: Modifie le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843665"
---
# <a name="lvm_setitemtext-message"></a>\_Message SETITEMTEXT LVM

Modifie le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Le membre **iSubItem** est l’index du sous-élément, ou il peut être égal à zéro pour définir l’étiquette de l’élément. Le membre **pszText** est l’adresse d’une chaîne se terminant par un caractère null qui contient le nouveau texte ; elle peut également avoir la **valeur null**. Le membre **pszText** peut également être LPSTR \_ TEXTCALLBACK pour indiquer un élément de rappel pour lequel la fenêtre parente stocke le texte. Dans ce cas, le contrôle List-View envoie au parent un code de notification [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) lorsqu’il a besoin du texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si vous envoyez ce message de manière explicite, il retourne **true** en cas de réussite ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) et **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





