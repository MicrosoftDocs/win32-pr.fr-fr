---
description: L’exemple suivant utilise la fonction VerifyVersionInfo pour déterminer si la suite de produits spécifiée est installée sur l’ordinateur local.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Détection d’une suite de produits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008886"
---
# <a name="detecting-a-product-suite"></a>Détection d’une suite de produits

L’exemple suivant utilise la fonction [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) pour déterminer si la suite de produits spécifiée est installée sur l’ordinateur local.

Cet exemple utilise le VER \_ et l’indicateur. Si deux indicateurs sont spécifiés dans le masque de suite, la fonction retourne **true** uniquement si les deux suites de produits sont présentes. Si l’exemple a été modifié pour utiliser le VER \_ ou l’indicateur, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) retourne la **valeur true** si l’une des suites de produits était présente.


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



 

 



