---
description: L’exemple suivant utilise la fonction ExitWindows pour fermer la session de l’utilisateur actuel.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Comment se déconnecter de l’utilisateur actuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951969"
---
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="7f092-103">Comment se déconnecter de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="7f092-103">How to Log Off the Current User</span></span>

<span data-ttu-id="7f092-104">L’exemple suivant utilise la fonction [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) pour fermer la session de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7f092-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="7f092-105">L’exemple suivant utilise la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) pour fermer la session de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7f092-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="7f092-106">L’application reçoit le message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) et affiche une boîte de dialogue qui vous demande s’il est correct de mettre fin à la session.</span><span class="sxs-lookup"><span data-stu-id="7f092-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="7f092-107">Si l’utilisateur clique sur **Oui**, le système ferme la session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f092-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="7f092-108">Si l’utilisateur clique sur **non**, la déconnexion est annulée.</span><span class="sxs-lookup"><span data-stu-id="7f092-108">If the user clicks **No**, the logoff is canceled.</span></span>

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a><span data-ttu-id="7f092-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f092-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f092-110">Fermeture de session</span><span class="sxs-lookup"><span data-stu-id="7f092-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



