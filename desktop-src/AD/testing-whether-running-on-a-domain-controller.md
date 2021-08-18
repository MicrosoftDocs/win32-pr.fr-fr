---
title: Test de l’exécution sur un contrôleur de domaine
description: le code suivant utilise la fonction VerifyVersionInfo pour déterminer si le processus appelant s’exécute sur un contrôleur de domaine Windows 2000 Server.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024587"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Test de l’exécution sur un contrôleur de domaine

le code suivant utilise la fonction [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) pour déterminer si le processus appelant s’exécute sur un contrôleur de domaine Windows 2000 Server. Votre programme d’installation de service peut utiliser ce test avant d’installer un service sous le compte LocalSystem. Si le test indique que vous êtes en cours d’exécution sur un contrôleur de domaine, vous installez le service pour qu’il s’exécute sous un compte d’utilisateur ou affichez une boîte de dialogue qui vous avertit des dangers liés à l’exécution en tant que LocalSystem sur un contrôleur de domaine (ce qui signifie que le service disposerait alors d’un accès illimité à Active Directory Domain Services, un contexte de sécurité extrêmement puissant


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



 

 