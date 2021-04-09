---
description: Si une application n’appelle pas la fonction SymInitialize avec le paramètre fInvadeProcess défini sur TRUE, elle doit charger les symboles pour un module lorsqu’ils sont requis.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Chargement d’un module de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110150"
---
# <a name="loading-a-symbol-module"></a><span data-ttu-id="1c186-103">Chargement d’un module de symboles</span><span class="sxs-lookup"><span data-stu-id="1c186-103">Loading a Symbol Module</span></span>

<span data-ttu-id="1c186-104">Si une application n’appelle pas la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) avec le paramètre *FInvadeProcess* défini sur **true**, elle doit charger les symboles pour un module lorsqu’ils sont requis.</span><span class="sxs-lookup"><span data-stu-id="1c186-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="1c186-105">Pour charger un module de symboles à la demande, l’application peut appeler la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) avec un chemin d’accès complet à un nom de module.</span><span class="sxs-lookup"><span data-stu-id="1c186-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="1c186-106">Une fois le module chargé, le gestionnaire de symboles charge les symboles immédiatement ou diffère le chargement, selon les options définies à l’aide de la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="1c186-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="1c186-107">Le code suivant charge un module de symboles.</span><span class="sxs-lookup"><span data-stu-id="1c186-107">The following code loads a symbol module.</span></span> <span data-ttu-id="1c186-108">Notez qu’il suppose que vous avez initialisé le gestionnaire de symboles à l’aide du code dans [initialisation du gestionnaire de symboles](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="1c186-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



<span data-ttu-id="1c186-109">Notez que *szImageName* peut être un chemin d’accès à n’importe quel module exécutable contenant des informations de débogage (. exe,. dll,. drv,. sys,. scr,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="1c186-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="1c186-110">En outre, *dwBaseAddr* est l’adresse de base du module de symboles à charger.</span><span class="sxs-lookup"><span data-stu-id="1c186-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="1c186-111">Si cette valeur est égale à 0, le gestionnaire de symboles obtient l’adresse de base à partir du module de symboles spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c186-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c186-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c186-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c186-113">Déchargement d’un module de symboles</span><span class="sxs-lookup"><span data-stu-id="1c186-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



