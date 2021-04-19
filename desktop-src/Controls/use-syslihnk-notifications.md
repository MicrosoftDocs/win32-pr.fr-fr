---
title: Utilisation des notifications SysLink
description: Deux messages de notification sont associés au contrôle SysLink \ 8212 ; un pour la souris (en- \_ cliquant sur Syslink) et l’autre pour le clavier (retour nm \_ ).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "106511277"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="57df7-103">Utilisation des notifications SysLink</span><span class="sxs-lookup"><span data-stu-id="57df7-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="57df7-104">Deux messages de notification sont associés au contrôle SysLink : un pour la souris (un[clic nm ( \_ Syslink)](nm-click-syslink.md)) et l’autre pour le clavier ([ \_ retour nm](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="57df7-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="57df7-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="57df7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="57df7-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="57df7-106">Technologies</span></span>

-   [<span data-ttu-id="57df7-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="57df7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="57df7-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="57df7-108">Prerequisites</span></span>

-   <span data-ttu-id="57df7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="57df7-109">C/C++</span></span>
-   <span data-ttu-id="57df7-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="57df7-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="57df7-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="57df7-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="57df7-112">Utiliser des notifications SysLink</span><span class="sxs-lookup"><span data-stu-id="57df7-112">Use SysLink Notifications</span></span>

<span data-ttu-id="57df7-113">L’exemple de code suivant montre comment traiter les notifications SysLink générées lorsque l’utilisateur clique sur l’un des deux liens dans l' [exemple précédent](create-syslink-controls.md).</span><span class="sxs-lookup"><span data-stu-id="57df7-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="57df7-114">Lorsque l’utilisateur clique sur l’URL Internet, la page Web associée s’ouvre dans le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="57df7-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="57df7-115">Quand l’utilisateur clique sur le lien hypertexte défini par l’application, une boîte de message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="57df7-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="57df7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57df7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57df7-117">Utilisation des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="57df7-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="57df7-118">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="57df7-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




