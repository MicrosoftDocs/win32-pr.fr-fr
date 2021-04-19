---
description: 'Comment créer des mailslots. Les mailslots sont pris en charge par trois fonctions spécialisées : CreateMailslot, GetMailslotInfo et SetMailslotInfo. Ces fonctions sont utilisées par le serveur mailslot.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Création d’un mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530909"
---
# <a name="creating-a-mailslot"></a><span data-ttu-id="65dfd-105">Création d’un mailslot</span><span class="sxs-lookup"><span data-stu-id="65dfd-105">Creating a Mailslot</span></span>

<span data-ttu-id="65dfd-106">Les mailslots sont pris en charge par trois fonctions spécialisées : [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)et [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span><span class="sxs-lookup"><span data-stu-id="65dfd-106">Mailslots are supported by three specialized functions: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo), and [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span></span> <span data-ttu-id="65dfd-107">Ces fonctions sont utilisées par le serveur mailslot.</span><span class="sxs-lookup"><span data-stu-id="65dfd-107">These functions are used by the mailslot server.</span></span>

<span data-ttu-id="65dfd-108">L’exemple de code suivant utilise la fonction [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) pour récupérer le descripteur d’un mailslot nommé « Sample \_ mailslot ».</span><span class="sxs-lookup"><span data-stu-id="65dfd-108">The following code sample uses the [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) function to retrieve the handle to a mailslot named "sample\_mailslot".</span></span> <span data-ttu-id="65dfd-109">L’exemple de code [écrit dans un mailslot](writing-to-a-mailslot.md) montre comment l’application cliente peut écrire sur ce mailslot.</span><span class="sxs-lookup"><span data-stu-id="65dfd-109">The code sample in [Writing to a Mailslot](writing-to-a-mailslot.md) shows how client application can write to this mailslot.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



<span data-ttu-id="65dfd-110">Pour créer un mailslot pouvant être hérité par les processus enfants, une application doit modifier la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) transmise en tant que dernier paramètre de [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span><span class="sxs-lookup"><span data-stu-id="65dfd-110">To create a mailslot that can be inherited by child processes, an application should change the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure passed as the last parameter of [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span></span> <span data-ttu-id="65dfd-111">Pour ce faire, l’application définit le membre **bInheritHandle** de cette structure sur **true** (le paramètre par défaut est **false**).</span><span class="sxs-lookup"><span data-stu-id="65dfd-111">To do this, the application sets the **bInheritHandle** member of this structure to **TRUE** (the default setting is **FALSE**).</span></span>

 

 
