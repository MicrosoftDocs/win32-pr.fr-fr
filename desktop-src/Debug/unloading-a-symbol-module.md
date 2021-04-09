---
description: Le code suivant décharge un module de symboles référencé par l’adresse du module BaseOfDll à l’aide de SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Déchargement d’un module de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b6fad0177fce36865e90dadf04bd563130789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861138"
---
# <a name="unloading-a-symbol-module"></a><span data-ttu-id="c4fdd-103">Déchargement d’un module de symboles</span><span class="sxs-lookup"><span data-stu-id="c4fdd-103">Unloading a Symbol Module</span></span>

<span data-ttu-id="c4fdd-104">Le code suivant décharge un module de symboles référencé par l’adresse du module BaseOfDll à l’aide de [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span><span class="sxs-lookup"><span data-stu-id="c4fdd-104">The following code unloads a symbol module referred to by the BaseOfDll module address using [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span></span>


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a><span data-ttu-id="c4fdd-105">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4fdd-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4fdd-106">Chargement d’un module de symboles</span><span class="sxs-lookup"><span data-stu-id="c4fdd-106">Loading a Symbol Module</span></span>](loading-a-symbol-module.md)
</dt> </dl>

 

 



