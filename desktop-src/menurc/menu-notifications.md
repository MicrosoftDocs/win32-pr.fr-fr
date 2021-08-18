---
title: Notifications de menu
description: Notifications de menu
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7370da93f430c62618b5d459e40bfa56cb7a9ff9f960f95eb6ce614cc7273e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734255"
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


## <a name="example"></a> Exemple

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

 




