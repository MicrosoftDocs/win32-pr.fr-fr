---
description: L’exemple suivant utilise la fonction ExitWindowsEx pour arrêter le système.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Comment arrêter le système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544849"
---
# <a name="how-to-shut-down-the-system"></a>Comment arrêter le système

L’exemple suivant utilise la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) pour arrêter le système. L’arrêt du vidage des tampons de fichiers sur le disque et amène le système à une condition dans laquelle il est possible de mettre hors tension l’ordinateur en toute sécurité. L’application doit d’abord activer le privilège de nom d’arrêt de la SE \_ \_ . Pour plus d’informations, consultez [privilèges](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



Le dernier paramètre de l’appel à [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indique que le système a été arrêté pour une mise à jour de planification du système d’exploitation. Pour plus d’informations, consultez codes de raison de l' [arrêt du système](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Arrêt en cours](shutting-down.md)
</dt> </dl>

 

 
