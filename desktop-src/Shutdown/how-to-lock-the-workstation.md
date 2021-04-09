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
# <a name="how-to-lock-the-workstation"></a>Verrouillage de la station de travail

L’exemple suivant verrouille la station de travail à l’aide de la fonction [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) . Le système affiche la boîte de dialogue **verrouiller la station de travail** . Le texte de la boîte de dialogue indique que la station de travail est en cours d’utilisation et qu’elle a été verrouillée par l’utilisateur.


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



Pour déterminer si la station de travail est verrouillée, vérifiez si votre fenêtre est visible.

La station de travail peut être déverrouillée par l’utilisateur ou par un administrateur. Pour déverrouiller le système, appuyez sur CTRL + ALT + SUPPR et connectez-vous. Pour recevoir une notification lorsque l’utilisateur se connecte, utilisez la fonction [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) pour s’inscrire afin de recevoir les messages de [**\_ \_ modification WM WTSSESSION**](../termserv/wm-wtssession-change.md) . Lorsque ce message est reçu, vérifiez si le paramètre *wParam* est égal au \_ verrou de session WTS \_ .

 

 
