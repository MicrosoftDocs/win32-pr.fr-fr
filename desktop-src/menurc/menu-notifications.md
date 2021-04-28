---
title: Notifications de menu
description: Notifications de menu
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112527"
---
# <a name="menu-notifications"></a><span data-ttu-id="92bfb-103">Notifications de menu</span><span class="sxs-lookup"><span data-stu-id="92bfb-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92bfb-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="92bfb-104">In This Section</span></span>

-   [<span data-ttu-id="92bfb-105">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="92bfb-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="92bfb-106">**WM \_ CONTEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="92bfb-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="92bfb-107">**\_ENTERMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="92bfb-108">**\_EXITMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="92bfb-109">**\_GETTITLEBARINFOEX WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="92bfb-110">**la \_ MENUCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="92bfb-111">**\_MENUDRAG WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="92bfb-112">**\_MENUGETOBJECT WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="92bfb-113">**\_MENURBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="92bfb-114">**\_NEXTMENU WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="92bfb-115">**\_UNINITMENUPOPUP WM**</span><span class="sxs-lookup"><span data-stu-id="92bfb-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="92bfb-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="92bfb-116">Example</span></span>

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
<span data-ttu-id="92bfb-117">Exemple tiré des [exemples Windows classiques](https://github.com/microsoft/Windows-classic-samples) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="92bfb-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




