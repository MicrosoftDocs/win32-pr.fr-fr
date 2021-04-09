---
description: Le gestionnaire de symboles est conçu pour effectuer le suivi de différents jeux de fichiers de symboles.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Initialisation du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110202"
---
# <a name="symbol-handler-initialization"></a><span data-ttu-id="eccb3-103">Initialisation du gestionnaire de symboles</span><span class="sxs-lookup"><span data-stu-id="eccb3-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="eccb3-104">Le gestionnaire de symboles est conçu pour effectuer le suivi de différents jeux de fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="eccb3-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="eccb3-105">Pour initialiser le gestionnaire de symboles, appelez la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="eccb3-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="eccb3-106">Le paramètre *hProcess* peut être un nombre arbitraire unique, une valeur retournée par la fonction [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou l’identificateur de tout processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eccb3-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="eccb3-107">Le paramètre *fInvadeProcess* indique si le gestionnaire de symboles doit énumérer les modules chargés par le processus et charger des symboles pour chacun de ses modules.</span><span class="sxs-lookup"><span data-stu-id="eccb3-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="eccb3-108">Si *fInvadeProcess* a la valeur **true**, le paramètre *hProcess* doit être la valeur retournée par **GetCurrentProcess** ou l’identificateur d’un processus existant.</span><span class="sxs-lookup"><span data-stu-id="eccb3-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="eccb3-109">Pour actualiser cette liste, utilisez la fonction [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .</span><span class="sxs-lookup"><span data-stu-id="eccb3-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="eccb3-110">L’utilisation de *fInvadeProcess* est un moyen simple de charger tous les fichiers de symboles d’un processus.</span><span class="sxs-lookup"><span data-stu-id="eccb3-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="eccb3-111">Toutefois, le gestionnaire de symboles ne tente pas de charger les symboles pour les modules qui sont ensuite chargés par la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="eccb3-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="eccb3-112">Dans ce cas, vous devez utiliser la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .</span><span class="sxs-lookup"><span data-stu-id="eccb3-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
