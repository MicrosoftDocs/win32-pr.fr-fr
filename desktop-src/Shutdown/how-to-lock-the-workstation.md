---
description: L’exemple suivant verrouille la station de travail à l’aide de la fonction LockWorkStation. Le système affiche la boîte de dialogue verrouiller la station de travail. Le texte de la boîte de dialogue indique que la station de travail est en cours d’utilisation et qu’elle a été verrouillée par l’utilisateur.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Verrouillage de la station de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865713"
---
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="5240c-105">Verrouillage de la station de travail</span><span class="sxs-lookup"><span data-stu-id="5240c-105">How to Lock the Workstation</span></span>

<span data-ttu-id="5240c-106">L’exemple suivant verrouille la station de travail à l’aide de la fonction [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) .</span><span class="sxs-lookup"><span data-stu-id="5240c-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="5240c-107">Le système affiche la boîte de dialogue **verrouiller la station de travail** .</span><span class="sxs-lookup"><span data-stu-id="5240c-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="5240c-108">Le texte de la boîte de dialogue indique que la station de travail est en cours d’utilisation et qu’elle a été verrouillée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5240c-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



<span data-ttu-id="5240c-109">Pour déterminer si la station de travail est verrouillée, vérifiez si votre fenêtre est visible.</span><span class="sxs-lookup"><span data-stu-id="5240c-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="5240c-110">La station de travail peut être déverrouillée par l’utilisateur ou par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="5240c-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="5240c-111">Pour déverrouiller le système, appuyez sur CTRL + ALT + SUPPR et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="5240c-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="5240c-112">Pour recevoir une notification lorsque l’utilisateur se connecte, utilisez la fonction [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) pour s’inscrire afin de recevoir les messages de [**\_ \_ modification WM WTSSESSION**](../termserv/wm-wtssession-change.md) .</span><span class="sxs-lookup"><span data-stu-id="5240c-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="5240c-113">Lorsque ce message est reçu, vérifiez si le paramètre *wParam* est égal au \_ verrou de session WTS \_ .</span><span class="sxs-lookup"><span data-stu-id="5240c-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
