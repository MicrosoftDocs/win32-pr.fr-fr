---
title: Message TB_ADDBUTTONS (commctrl. h)
description: Ajoute un ou plusieurs boutons à une barre d’outils.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942914"
---
# <a name="tb_addbuttons-message"></a>TO \_ ADDBUTTONS message

Ajoute un ou plusieurs boutons à une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de boutons à ajouter.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de structures [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui contiennent des informations sur les boutons à ajouter. Le tableau doit contenir le même nombre d’éléments que les boutons spécifiés par *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Si la barre d’outils a été créée à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , vous devez envoyer le message [**to \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) à la barre d’outils avant d’envoyer **to \_ ADDBUTTONS**.

Consultez [**to \_ SETIMAGELIST**](tb-setimagelist.md) pour savoir comment assigner des bitmaps à des boutons de barre d’outils à partir d’une ou plusieurs listes d’images.

## <a name="examples"></a>Exemples

L’exemple de code suivant ajoute trois boutons à une barre d’outils, à l’aide de la bitmap système standard pour les boutons de vue. Le message [**to \_ ADDBITMAP**](tb-addbitmap.md) retourne l’index de la première image de bouton dans la liste d’images. Les images individuelles sont identifiées par leurs décalages par rapport à cette valeur.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ ADDBUTTONSW** (Unicode) et **to \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Valeurs d’index d’image du bouton standard de la barre d’outils**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

