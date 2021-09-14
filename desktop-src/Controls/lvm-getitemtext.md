---
title: Message LVM_GETITEMTEXT (commctrl. h)
description: Récupère le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemText.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999815"
---
# <a name="lvm_getitemtext-message"></a>\_Message GETITEMTEXT LVM

Récupère le texte d’un élément ou d’un sous-élément de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Pour récupérer le texte de l’élément, affectez à **iSubItem** la valeur zéro. Pour récupérer le texte d’un sous-élément, définissez **iSubItem** sur l’index du sous-élément. Le membre **pszText** pointe vers une mémoire tampon qui reçoit le texte. Le membre **cchTextMax** spécifie le nombre de caractères dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si vous envoyez ce message de manière explicite, il retourne le nombre de caractères dans le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="remarks"></a>Notes

Vous pouvez également envoyer ce message en appelant la macro [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . Toutefois, cette macro ne retourne pas la longueur de la chaîne.

**LVM \_ GETITEMTEXT** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) et **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





