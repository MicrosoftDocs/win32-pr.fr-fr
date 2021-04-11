---
description: Le code suivant montre comment initialiser le gestionnaire de symboles.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Initialisation du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950441"
---
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="6eb5d-103">Initialisation du gestionnaire de symboles</span><span class="sxs-lookup"><span data-stu-id="6eb5d-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="6eb5d-104">Le code suivant montre comment initialiser le gestionnaire de symboles.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="6eb5d-105">La fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) diffère le chargement de symboles jusqu’à ce que les informations de symbole soient demandées.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="6eb5d-106">Le code charge les symboles pour chaque module dans le processus spécifié en passant la valeur **true** pour le paramètre *bInvade* de la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="6eb5d-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="6eb5d-107">(Cette fonction appelle la fonction [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) pour chaque module que le processus a mappé dans son espace d’adressage.)</span><span class="sxs-lookup"><span data-stu-id="6eb5d-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="6eb5d-108">Si le processus spécifié n’est pas le processus qui a appelé [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), le code passe un identificateur de processus comme premier paramètre de **syminitialize**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="6eb5d-109">La spécification de **null** comme deuxième paramètre de [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indique que le gestionnaire de symboles doit utiliser le chemin de recherche par défaut pour localiser les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="6eb5d-110">Pour plus d’informations sur la façon dont le gestionnaire de symboles localise les fichiers de symboles ou sur la façon dont une application peut spécifier un chemin de recherche de symboles, consultez [chemins d'](symbol-paths.md)accès aux symboles.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



