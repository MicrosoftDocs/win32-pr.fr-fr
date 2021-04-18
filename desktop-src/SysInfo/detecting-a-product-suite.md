---
description: L’exemple suivant utilise la fonction VerifyVersionInfo pour déterminer si la suite de produits spécifiée est installée sur l’ordinateur local.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Détection d’une suite de produits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520199"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="2852a-103">Détection d’une suite de produits</span><span class="sxs-lookup"><span data-stu-id="2852a-103">Detecting a Product Suite</span></span>

<span data-ttu-id="2852a-104">L’exemple suivant utilise la fonction [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) pour déterminer si la suite de produits spécifiée est installée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2852a-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="2852a-105">Cet exemple utilise le VER \_ et l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="2852a-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="2852a-106">Si deux indicateurs sont spécifiés dans le masque de suite, la fonction retourne **true** uniquement si les deux suites de produits sont présentes.</span><span class="sxs-lookup"><span data-stu-id="2852a-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="2852a-107">Si l’exemple a été modifié pour utiliser le VER \_ ou l’indicateur, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) retourne la **valeur true** si l’une des suites de produits était présente.</span><span class="sxs-lookup"><span data-stu-id="2852a-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



