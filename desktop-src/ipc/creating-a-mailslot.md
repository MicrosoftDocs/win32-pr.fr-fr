---
description: 'Comment créer des mailslots. Les mailslots sont pris en charge par trois fonctions spécialisées : CreateMailslot, GetMailslotInfo et SetMailslotInfo. Ces fonctions sont utilisées par le serveur mailslot.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Création d’un mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebdc255772c8dbe06ff3a1258c5d2176f595d4e6e0a162bfbe662ce15838881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350419"
---
# <a name="creating-a-mailslot"></a>Création d’un mailslot

Les mailslots sont pris en charge par trois fonctions spécialisées : [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)et [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo). Ces fonctions sont utilisées par le serveur mailslot.

L’exemple de code suivant utilise la fonction [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) pour récupérer le descripteur d’un mailslot nommé « Sample \_ mailslot ». L’exemple de code [écrit dans un mailslot](writing-to-a-mailslot.md) montre comment l’application cliente peut écrire sur ce mailslot.


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



Pour créer un mailslot pouvant être hérité par les processus enfants, une application doit modifier la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) transmise en tant que dernier paramètre de [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). Pour ce faire, l’application définit le membre **bInheritHandle** de cette structure sur **true** (le paramètre par défaut est **false**).

 

 
