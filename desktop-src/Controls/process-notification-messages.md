---
title: Comment traiter des messages de notification
description: Une feuille de propriétés envoie \_ des messages de notification WM pour récupérer des informations à partir des pages et notifier les pages des actions de l’utilisateur.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724278"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="3737b-103">Comment traiter des messages de notification</span><span class="sxs-lookup"><span data-stu-id="3737b-103">How to Process Notification Messages</span></span>

<span data-ttu-id="3737b-104">Une feuille de propriétés envoie des messages de [**\_ notification WM**](wm-notify.md) pour récupérer des informations à partir des pages et notifier les pages des actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3737b-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="3737b-105">Le paramètre *lParam* du message est l’adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , qui contient le descripteur de la boîte de dialogue de la feuille de propriétés, le handle de la boîte de dialogue de la page et un code de notification.</span><span class="sxs-lookup"><span data-stu-id="3737b-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="3737b-106">La page doit répondre à certains messages de notification en affectant \_ à la valeur MSGRESULT de la page la valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="3737b-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3737b-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="3737b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3737b-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="3737b-108">Technologies</span></span>

-   [<span data-ttu-id="3737b-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="3737b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3737b-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3737b-110">Prerequisites</span></span>

-   <span data-ttu-id="3737b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3737b-111">C/C++</span></span>
-   <span data-ttu-id="3737b-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="3737b-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3737b-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="3737b-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="3737b-114">Traiter les messages de notification</span><span class="sxs-lookup"><span data-stu-id="3737b-114">Process Notification Messages</span></span>

<span data-ttu-id="3737b-115">L’exemple suivant est un fragment de code de la procédure de boîte de dialogue pour une page.</span><span class="sxs-lookup"><span data-stu-id="3737b-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="3737b-116">Il montre comment traiter le code de notification [ \_ d’aide PSN](psn-help.md) .</span><span class="sxs-lookup"><span data-stu-id="3737b-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="3737b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3737b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3737b-118">Utilisation des feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="3737b-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="3737b-119">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3737b-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




