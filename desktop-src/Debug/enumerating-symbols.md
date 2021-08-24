---
description: Le code suivant affiche le nom, l’adresse et la taille de chaque symbole chargé dans le module spécifié.
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: Énumération des symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 041768d46fec2aada74ebef37fdf5ffbb719b7c691a5e037a0f2f0532390d54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692029"
---
# <a name="enumerating-symbols"></a>Énumération des symboles

Le code suivant affiche le nom, l’adresse et la taille de chaque symbole chargé dans le module spécifié. La fonction [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) nécessite une fonction de rappel, qui est appelée une fois pour chaque module chargé. Dans cet exemple, EnumSymProc est une implémentation de la fonction de rappel.


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



