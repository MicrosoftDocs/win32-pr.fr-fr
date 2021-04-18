---
title: Message LVM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512600"
---
# <a name="lvm_insertitem-message"></a>\_Message INSERTITEM LVM

Insère un nouvel élément dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui spécifie les attributs de l’élément de vue de liste. Utilisez le membre **iItem** pour spécifier l’index de base zéro auquel le nouvel élément doit être inséré. Si cette valeur est supérieure au nombre d’éléments actuellement contenus dans le ListView, le nouvel élément est ajouté à la fin de la liste et reçoit l’index correct. Examinez la valeur de retour du message pour déterminer l’index réel affecté à l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index du nouvel élément en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Vous ne pouvez pas utiliser [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou **LVM \_ InsertItem** pour insérer des sous-éléments. Le membre **iSubItem** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) doit être égal à zéro. Pour plus d’informations sur la définition des sous-éléments, consultez [**\_ SETITEM LVM**](lvm-setitem.md) .

Si un contrôle List-View a le style [**LVS \_ ex \_ checkboxs**](extended-list-view-styles.md) défini, toute valeur placée dans les bits 12 à 15 du membre **State** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sera ignorée. Lorsqu’un élément est ajouté avec cet ensemble de styles, il est toujours défini sur l’état désactivé.

Si un contrôle List-View a le style de fenêtre [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , un **message \_ INSERTITEM de LVM** échoue si vous essayez d’insérer un élément dont \_ la valeur de LPSTR TEXTCALLBACK est la valeur de son membre **pszText** .

Le **message \_ INSERTITEM du LVM** insère le nouvel élément à la position appropriée dans l’ordre de tri si les conditions suivantes sont respectées :

-   Vous utilisez l’un des styles LVS \_ SORTXXX.
-   Vous n’utilisez pas le style [**LVS \_ OwnerDraw**](list-view-window-styles.md) .
-   Le membre **pszText** de la structure vers laquelle pointe **pItem** n’a pas la valeur LPSTR \_ TEXTCALLBACK.

Si la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) ne contient pas LVIF \_ GROUPID dans le membre **Mask** , la valeur du membre **iGroupId** est I \_ GROUPIDCALLBACK par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) et **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





