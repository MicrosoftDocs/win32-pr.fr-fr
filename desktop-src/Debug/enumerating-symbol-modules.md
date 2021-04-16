---
description: Le code suivant répertorie les modules qui ont été chargés par la fonction SymLoadModule64 ou SymInitialize.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Énumération des modules de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482728"
---
# <a name="enumerating-symbol-modules"></a><span data-ttu-id="77101-103">Énumération des modules de symboles</span><span class="sxs-lookup"><span data-stu-id="77101-103">Enumerating Symbol Modules</span></span>

<span data-ttu-id="77101-104">Le code suivant répertorie les modules qui ont été chargés par la fonction [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) ou [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="77101-104">The following code lists the modules that have been loaded by the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="77101-105">La fonction [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) nécessite une fonction de rappel, qui sera appelée une fois pour chaque module chargé.</span><span class="sxs-lookup"><span data-stu-id="77101-105">The [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) function requires a callback function, which will be called once for each module loaded.</span></span> <span data-ttu-id="77101-106">Dans cet exemple, EnumModules est une implémentation de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="77101-106">In this example, EnumModules is an implementation of the callback function.</span></span> <span data-ttu-id="77101-107">L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="77101-107">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



