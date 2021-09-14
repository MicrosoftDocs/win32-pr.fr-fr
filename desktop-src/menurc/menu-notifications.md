---
title: Notifications de menu
description: Notifications de menu
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235716"
---
# <a name="menu-notifications"></a>Notifications de menu

## <a name="in-this-section"></a>Dans cette section

-   [**WM, \_ commande**](wm-command.md)
-   [**WM \_ CONTEXTMENU**](wm-contextmenu.md)
-   [**\_ENTERMENULOOP WM**](wm-entermenuloop.md)
-   [**\_EXITMENULOOP WM**](wm-exitmenuloop.md)
-   [**\_GETTITLEBARINFOEX WM**](wm-gettitlebarinfoex.md)
-   [**la \_ MENUCOMMAND WM**](wm-menucommand.md)
-   [**\_MENUDRAG WM**](wm-menudrag.md)
-   [**\_MENUGETOBJECT WM**](wm-menugetobject.md)
-   [**\_MENURBUTTONUP WM**](wm-menurbuttonup.md)
-   [**\_NEXTMENU WM**](wm-nextmenu.md)
-   [**\_UNINITMENUPOPUP WM**](wm-uninitmenupopup.md)


## <a name="example"></a>Exemple

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
exemple tiré d' [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples) sur GitHub.

 




