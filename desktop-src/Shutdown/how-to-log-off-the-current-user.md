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
# <a name="how-to-log-off-the-current-user"></a>Comment se déconnecter de l’utilisateur actuel

L’exemple suivant utilise la fonction [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) pour fermer la session de l’utilisateur actuel.

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

L’exemple suivant utilise la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) pour fermer la session de l’utilisateur actuel.

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

L’application reçoit le message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) et affiche une boîte de dialogue qui vous demande s’il est correct de mettre fin à la session. Si l’utilisateur clique sur **Oui**, le système ferme la session de l’utilisateur. Si l’utilisateur clique sur **non**, la déconnexion est annulée.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fermeture de session](logging-off.md)
</dt> </dl>

 

 



