---
title: Test de l’exécution sur un contrôleur de domaine
description: Le code suivant utilise la fonction VerifyVersionInfo pour déterminer si le processus appelant s’exécute sur un contrôleur de domaine du serveur Windows 2000.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101412"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="6ca09-103">Test de l’exécution sur un contrôleur de domaine</span><span class="sxs-lookup"><span data-stu-id="6ca09-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="6ca09-104">Le code suivant utilise la fonction [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) pour déterminer si le processus appelant s’exécute sur un contrôleur de domaine du serveur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6ca09-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="6ca09-105">Votre programme d’installation de service peut utiliser ce test avant d’installer un service sous le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="6ca09-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="6ca09-106">Si le test indique que vous êtes en cours d’exécution sur un contrôleur de domaine, vous installez le service pour qu’il s’exécute sous un compte d’utilisateur ou affichez une boîte de dialogue qui vous avertit des dangers liés à l’exécution en tant que LocalSystem sur un contrôleur de domaine (ce qui signifie que le service disposerait alors d’un accès illimité à Active Directory Domain Services, un contexte de sécurité extrêmement puissant</span><span class="sxs-lookup"><span data-stu-id="6ca09-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 