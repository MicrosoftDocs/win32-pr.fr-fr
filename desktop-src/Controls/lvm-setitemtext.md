---
title: Message LVM_SETITEMTEXT (commctrl. h)
description: Modifie le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312653"
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

## <a name="return-value"></a>Valeur de retour

Si vous envoyez ce message de manière explicite, il retourne **true** en cas de réussite ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) et **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





