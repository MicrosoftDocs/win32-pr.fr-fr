---
description: Le cas échéant, la bibliothèque DbgHelp a été étendue pour prendre en charge les fenêtres 32 et 64 bits.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Plateforme d'appui améliorée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523668"
---
# <a name="updated-platform-support"></a><span data-ttu-id="dcf8b-103">Plateforme d'appui améliorée</span><span class="sxs-lookup"><span data-stu-id="dcf8b-103">Updated Platform Support</span></span>

<span data-ttu-id="dcf8b-104">Le cas échéant, la bibliothèque DbgHelp a été étendue pour prendre en charge les fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="dcf8b-105">Les définitions de fonction et de structure d’origine sont toujours dans DbgHelp. h, mais des versions mises à jour de ces définitions sont compatibles avec Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="dcf8b-106">Si vous utilisez les fonctions mises à jour dans votre code, elles peuvent être compilées pour les fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="dcf8b-107">Votre code sera également plus efficace, car les fonctions d’origine appellent simplement les fonctions mises à jour pour effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="dcf8b-108">Par exemple, DbgHelp. h contient des définitions pour **SymUnloadModule** (fonction d’origine) et **SymUnloadModule64** (fonction mise à jour).</span><span class="sxs-lookup"><span data-stu-id="dcf8b-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="dcf8b-109">Ces définitions sont presque identiques, mais utilisent des types différents pour le paramètre *BaseOfDll* .</span><span class="sxs-lookup"><span data-stu-id="dcf8b-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="dcf8b-110">(**SymUnloadModule** utilise le type **DWORD** , tandis que **SymUnloadModule64** utilise le type **DWORD64** .) Si vous écrivez votre code pour utiliser **SymUnloadModule64**, il peut être compilé pour les fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="dcf8b-111">Le code est également plus efficace que s’il s’agissait d’appeler **SymUnloadModule**.</span><span class="sxs-lookup"><span data-stu-id="dcf8b-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="dcf8b-112">La liste suivante répertorie les fonctions mises à jour :</span><span class="sxs-lookup"><span data-stu-id="dcf8b-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="dcf8b-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="dcf8b-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="dcf8b-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="dcf8b-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="dcf8b-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="dcf8b-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="dcf8b-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="dcf8b-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="dcf8b-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="dcf8b-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="dcf8b-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="dcf8b-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="dcf8b-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="dcf8b-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="dcf8b-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="dcf8b-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="dcf8b-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="dcf8b-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="dcf8b-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="dcf8b-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="dcf8b-133">La liste suivante répertorie les structures mises à jour :</span><span class="sxs-lookup"><span data-stu-id="dcf8b-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="dcf8b-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="dcf8b-135">**\_Symbole différé imagehlp \_ \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="dcf8b-136">**\_SYMBOL64 en double \_**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="dcf8b-137">**\_LINE64 imagehlp**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="dcf8b-138">**\_MODULE64 imagehlp**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="dcf8b-139">**\_SYMBOL64 imagehlp**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="dcf8b-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="dcf8b-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="dcf8b-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



