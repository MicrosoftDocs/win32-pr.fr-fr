---
description: L’exemple suivant redémarre le système local à l’aide de la fonction InitiateSystemShutdown.
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: Affichage de la boîte de dialogue d’arrêt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521562"
---
# <a name="displaying-the-shutdown-dialog-box"></a>Affichage de la boîte de dialogue d’arrêt

L’exemple suivant redémarre le système local à l’aide de la fonction [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) . Le système affiche une boîte de dialogue avec un message personnalisé et un message à l’utilisateur pour fermer les applications au cours de l’intervalle de délai d’attente spécifié (30 secondes). Lorsque l’intervalle de délai d’attente est écoulé, le système est redémarré.

L’application doit activer le privilège de nom d’arrêt du SE \_ avant d' \_ appeler [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna). Pour plus d’informations, consultez [privilèges](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



Si la fonction [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) est exécutée dans le délai d’attente spécifié par [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), le système ne s’arrête pas. Par exemple, si PreventSystemShutdown est appelé après MySystemShutdown, le système ferme la boîte de dialogue et ne redémarre pas le système.


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
