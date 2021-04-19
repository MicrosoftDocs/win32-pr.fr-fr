---
description: Le code suivant montre comment récupérer un nom de symbole non décoré à partir d’un nom de symbole à l’aide de UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Récupération de noms de symboles non décorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514363"
---
# <a name="retrieving-undecorated-symbol-names"></a><span data-ttu-id="ca557-103">Récupération de noms de symboles non décorés</span><span class="sxs-lookup"><span data-stu-id="ca557-103">Retrieving Undecorated Symbol Names</span></span>

<span data-ttu-id="ca557-104">Le code suivant montre comment récupérer un nom de symbole non décoré à partir d’un nom de symbole à l’aide de [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span><span class="sxs-lookup"><span data-stu-id="ca557-104">The following code demonstrates how to retrieve an undecorated symbol name from a symbol name using [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span></span> <span data-ttu-id="ca557-105">Le nom décoré est stocké dans `szName` .</span><span class="sxs-lookup"><span data-stu-id="ca557-105">The decorated name is stored in `szName`.</span></span> <span data-ttu-id="ca557-106">L’exemple suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="ca557-106">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



