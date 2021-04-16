---
description: Voici les fonctions DbgHelp.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Fonctions DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db65e46fe407b26b1a6ec9ae3cb8d5d7301d5821
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524071"
---
# <a name="dbghelp-functions"></a><span data-ttu-id="035b3-103">Fonctions DbgHelp</span><span class="sxs-lookup"><span data-stu-id="035b3-103">DbgHelp Functions</span></span>

<span data-ttu-id="035b3-104">Voici les fonctions DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="035b3-104">The following are the DbgHelp functions.</span></span>

## <a name="general"></a><span data-ttu-id="035b3-105">Général</span><span class="sxs-lookup"><span data-stu-id="035b3-105">General</span></span>

<span data-ttu-id="035b3-106">Les fonctions d’assistance générales sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="035b3-106">The following are general helper functions:</span></span>

<dl>

[<span data-ttu-id="035b3-107">**EnumDirTree**</span><span class="sxs-lookup"><span data-stu-id="035b3-107">**EnumDirTree**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[<span data-ttu-id="035b3-108">**ImagehlpApiVersion**</span><span class="sxs-lookup"><span data-stu-id="035b3-108">**ImagehlpApiVersion**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[<span data-ttu-id="035b3-109">**ImagehlpApiVersionEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-109">**ImagehlpApiVersionEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[<span data-ttu-id="035b3-110">**MakeSureDirectoryPathExists**</span><span class="sxs-lookup"><span data-stu-id="035b3-110">**MakeSureDirectoryPathExists**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[<span data-ttu-id="035b3-111">**SearchTreeForFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-111">**SearchTreeForFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a><span data-ttu-id="035b3-112">Débogueur</span><span class="sxs-lookup"><span data-stu-id="035b3-112">Debugger</span></span>

<span data-ttu-id="035b3-113">Les fonctions de service de débogage sont les fonctions les plus adaptées à une utilisation par un débogueur ou le code de débogage dans une application.</span><span class="sxs-lookup"><span data-stu-id="035b3-113">The debugging service functions are the functions most suited for use by a debugger or the debugging code in an application.</span></span> <span data-ttu-id="035b3-114">Ces fonctions peuvent être utilisées conjointement avec les fonctions de gestionnaire de symboles pour une utilisation plus facile.</span><span class="sxs-lookup"><span data-stu-id="035b3-114">These functions can be used in concert with the symbol handler functions for easier use.</span></span>

<dl>

[<span data-ttu-id="035b3-115">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="035b3-115">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="035b3-116">**EnumerateLoadedModulesEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-116">**EnumerateLoadedModulesEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[<span data-ttu-id="035b3-117">**FindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-117">**FindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[<span data-ttu-id="035b3-118">**FindDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-118">**FindDebugInfoFileEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[<span data-ttu-id="035b3-119">**FindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="035b3-119">**FindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[<span data-ttu-id="035b3-120">**FindExecutableImageEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-120">**FindExecutableImageEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[<span data-ttu-id="035b3-121">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="035b3-121">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="035b3-122">**SymSetParentWindow**</span><span class="sxs-lookup"><span data-stu-id="035b3-122">**SymSetParentWindow**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[<span data-ttu-id="035b3-123">**UnDecorateSymbolName**</span><span class="sxs-lookup"><span data-stu-id="035b3-123">**UnDecorateSymbolName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a><span data-ttu-id="035b3-124">Accès aux images</span><span class="sxs-lookup"><span data-stu-id="035b3-124">Image Access</span></span>

<span data-ttu-id="035b3-125">Les fonctions d’accès à l’image accèdent aux données d’une image exécutable.</span><span class="sxs-lookup"><span data-stu-id="035b3-125">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="035b3-126">Les fonctions fournissent un accès de haut niveau à la base d’images et un accès très spécifique aux parties les plus courantes des données d’une image.</span><span class="sxs-lookup"><span data-stu-id="035b3-126">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="035b3-127">**GetTimestampForLoadedLibrary**</span><span class="sxs-lookup"><span data-stu-id="035b3-127">**GetTimestampForLoadedLibrary**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[<span data-ttu-id="035b3-128">**Échec imagedirectoryentrytodata**</span><span class="sxs-lookup"><span data-stu-id="035b3-128">**ImageDirectoryEntryToData**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[<span data-ttu-id="035b3-129">**ImageDirectoryEntryToDataEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-129">**ImageDirectoryEntryToDataEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[<span data-ttu-id="035b3-130">**ImageNtHeader**</span><span class="sxs-lookup"><span data-stu-id="035b3-130">**ImageNtHeader**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[<span data-ttu-id="035b3-131">**ImageRvaToSection**</span><span class="sxs-lookup"><span data-stu-id="035b3-131">**ImageRvaToSection**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[<span data-ttu-id="035b3-132">**ImageRvaToVa**</span><span class="sxs-lookup"><span data-stu-id="035b3-132">**ImageRvaToVa**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a><span data-ttu-id="035b3-133">Gestionnaire de symboles</span><span class="sxs-lookup"><span data-stu-id="035b3-133">Symbol Handler</span></span>

<span data-ttu-id="035b3-134">Les fonctions de [Gestionnaire de symboles](symbol-handling.md) offrent aux applications un accès facile et portable aux informations de débogage symboliques d’une image.</span><span class="sxs-lookup"><span data-stu-id="035b3-134">The [symbol handler](symbol-handling.md) functions give applications easy and portable access to the symbolic debugging information of an image.</span></span> <span data-ttu-id="035b3-135">Ces fonctions doivent être utilisées exclusivement pour garantir l’accès aux informations symboliques.</span><span class="sxs-lookup"><span data-stu-id="035b3-135">These functions should be used exclusively to ensure access to symbolic information.</span></span> <span data-ttu-id="035b3-136">Cela est nécessaire, car ces fonctions isolent l’application du format des symboles.</span><span class="sxs-lookup"><span data-stu-id="035b3-136">This is necessary because these functions isolate the application from the symbol format.</span></span>

<dl>

[<span data-ttu-id="035b3-137">**SymAddSourceStream**</span><span class="sxs-lookup"><span data-stu-id="035b3-137">**SymAddSourceStream**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[<span data-ttu-id="035b3-138">**SymAddSymbol**</span><span class="sxs-lookup"><span data-stu-id="035b3-138">**SymAddSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[<span data-ttu-id="035b3-139">**SymCleanup**</span><span class="sxs-lookup"><span data-stu-id="035b3-139">**SymCleanup**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[<span data-ttu-id="035b3-140">**SymDeleteSymbol**</span><span class="sxs-lookup"><span data-stu-id="035b3-140">**SymDeleteSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[<span data-ttu-id="035b3-141">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="035b3-141">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="035b3-142">**SymEnumLines**</span><span class="sxs-lookup"><span data-stu-id="035b3-142">**SymEnumLines**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[<span data-ttu-id="035b3-143">**SymEnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="035b3-143">**SymEnumProcesses**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[<span data-ttu-id="035b3-144">**SymEnumSourceFiles**</span><span class="sxs-lookup"><span data-stu-id="035b3-144">**SymEnumSourceFiles**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[<span data-ttu-id="035b3-145">**SymEnumSourceLines**</span><span class="sxs-lookup"><span data-stu-id="035b3-145">**SymEnumSourceLines**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[<span data-ttu-id="035b3-146">**SymEnumSymbols**</span><span class="sxs-lookup"><span data-stu-id="035b3-146">**SymEnumSymbols**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[<span data-ttu-id="035b3-147">**SymEnumSymbolsForAddr**</span><span class="sxs-lookup"><span data-stu-id="035b3-147">**SymEnumSymbolsForAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[<span data-ttu-id="035b3-148">**SymEnumTypes**</span><span class="sxs-lookup"><span data-stu-id="035b3-148">**SymEnumTypes**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[<span data-ttu-id="035b3-149">**SymEnumTypesByName**</span><span class="sxs-lookup"><span data-stu-id="035b3-149">**SymEnumTypesByName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[<span data-ttu-id="035b3-150">**SymFindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-150">**SymFindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[<span data-ttu-id="035b3-151">**SymFindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="035b3-151">**SymFindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[<span data-ttu-id="035b3-152">**SymFindFileInPath**</span><span class="sxs-lookup"><span data-stu-id="035b3-152">**SymFindFileInPath**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[<span data-ttu-id="035b3-153">**SymFromAddr**</span><span class="sxs-lookup"><span data-stu-id="035b3-153">**SymFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[<span data-ttu-id="035b3-154">**SymFromIndex**</span><span class="sxs-lookup"><span data-stu-id="035b3-154">**SymFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[<span data-ttu-id="035b3-155">**SymFromName**</span><span class="sxs-lookup"><span data-stu-id="035b3-155">**SymFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[<span data-ttu-id="035b3-156">**SymFromToken**</span><span class="sxs-lookup"><span data-stu-id="035b3-156">**SymFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[<span data-ttu-id="035b3-157">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="035b3-157">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="035b3-158">**SymGetFileLineOffsets64**</span><span class="sxs-lookup"><span data-stu-id="035b3-158">**SymGetFileLineOffsets64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[<span data-ttu-id="035b3-159">**SymGetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="035b3-159">**SymGetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[<span data-ttu-id="035b3-160">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="035b3-160">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="035b3-161">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="035b3-161">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="035b3-162">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="035b3-162">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="035b3-163">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="035b3-163">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="035b3-164">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="035b3-164">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="035b3-165">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="035b3-165">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="035b3-166">**SymGetOmaps**</span><span class="sxs-lookup"><span data-stu-id="035b3-166">**SymGetOmaps**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[<span data-ttu-id="035b3-167">**SymGetOptions**</span><span class="sxs-lookup"><span data-stu-id="035b3-167">**SymGetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[<span data-ttu-id="035b3-168">**SymGetScope**</span><span class="sxs-lookup"><span data-stu-id="035b3-168">**SymGetScope**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[<span data-ttu-id="035b3-169">**SymGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="035b3-169">**SymGetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[<span data-ttu-id="035b3-170">**SymGetSymbolFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-170">**SymGetSymbolFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[<span data-ttu-id="035b3-171">**SymGetTypeFromName**</span><span class="sxs-lookup"><span data-stu-id="035b3-171">**SymGetTypeFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[<span data-ttu-id="035b3-172">**SymGetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="035b3-172">**SymGetTypeInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[<span data-ttu-id="035b3-173">**SymGetTypeInfoEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-173">**SymGetTypeInfoEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[<span data-ttu-id="035b3-174">**SymInitialize**</span><span class="sxs-lookup"><span data-stu-id="035b3-174">**SymInitialize**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[<span data-ttu-id="035b3-175">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="035b3-175">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="035b3-176">**SymLoadModuleEx**</span><span class="sxs-lookup"><span data-stu-id="035b3-176">**SymLoadModuleEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[<span data-ttu-id="035b3-177">**SymMatchFileName**</span><span class="sxs-lookup"><span data-stu-id="035b3-177">**SymMatchFileName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[<span data-ttu-id="035b3-178">**SymMatchString**</span><span class="sxs-lookup"><span data-stu-id="035b3-178">**SymMatchString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[<span data-ttu-id="035b3-179">**SymNext**</span><span class="sxs-lookup"><span data-stu-id="035b3-179">**SymNext**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[<span data-ttu-id="035b3-180">**SymPrev**</span><span class="sxs-lookup"><span data-stu-id="035b3-180">**SymPrev**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[<span data-ttu-id="035b3-181">**SymRefreshModuleList**</span><span class="sxs-lookup"><span data-stu-id="035b3-181">**SymRefreshModuleList**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[<span data-ttu-id="035b3-182">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="035b3-182">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="035b3-183">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="035b3-183">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="035b3-184">**SymSearch**</span><span class="sxs-lookup"><span data-stu-id="035b3-184">**SymSearch**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[<span data-ttu-id="035b3-185">**SymSetContext**</span><span class="sxs-lookup"><span data-stu-id="035b3-185">**SymSetContext**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[<span data-ttu-id="035b3-186">**SymSetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="035b3-186">**SymSetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[<span data-ttu-id="035b3-187">**SymSetOptions**</span><span class="sxs-lookup"><span data-stu-id="035b3-187">**SymSetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[<span data-ttu-id="035b3-188">**SymSetScopeFromAddr**</span><span class="sxs-lookup"><span data-stu-id="035b3-188">**SymSetScopeFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[<span data-ttu-id="035b3-189">**SymSetScopeFromIndex**</span><span class="sxs-lookup"><span data-stu-id="035b3-189">**SymSetScopeFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[<span data-ttu-id="035b3-190">**SymSetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="035b3-190">**SymSetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[<span data-ttu-id="035b3-191">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="035b3-191">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="035b3-192">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="035b3-192">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a><span data-ttu-id="035b3-193">Serveur de symboles</span><span class="sxs-lookup"><span data-stu-id="035b3-193">Symbol Server</span></span>

<span data-ttu-id="035b3-194">Le [serveur de symboles](symbol-servers-and-symbol-stores.md) permet aux débogueurs de récupérer automatiquement les fichiers de symboles appropriés sans les noms de produits, les mises en production ou les numéros de Build.</span><span class="sxs-lookup"><span data-stu-id="035b3-194">The [symbol server](symbol-servers-and-symbol-stores.md) enables debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="035b3-195">Les fonctions suivantes sont utilisées avec le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="035b3-195">The following functions are used with the symbol server.</span></span>

<dl>

[<span data-ttu-id="035b3-196">**SymSrvDeltaName**</span><span class="sxs-lookup"><span data-stu-id="035b3-196">**SymSrvDeltaName**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[<span data-ttu-id="035b3-197">**SymSrvGetFileIndexes**</span><span class="sxs-lookup"><span data-stu-id="035b3-197">**SymSrvGetFileIndexes**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[<span data-ttu-id="035b3-198">**SymSrvGetFileIndexInfo**</span><span class="sxs-lookup"><span data-stu-id="035b3-198">**SymSrvGetFileIndexInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[<span data-ttu-id="035b3-199">**SymSrvGetFileIndexString**</span><span class="sxs-lookup"><span data-stu-id="035b3-199">**SymSrvGetFileIndexString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[<span data-ttu-id="035b3-200">**SymSrvGetSupplement**</span><span class="sxs-lookup"><span data-stu-id="035b3-200">**SymSrvGetSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[<span data-ttu-id="035b3-201">**SymSrvIsStore**</span><span class="sxs-lookup"><span data-stu-id="035b3-201">**SymSrvIsStore**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[<span data-ttu-id="035b3-202">**SymSrvStoreFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-202">**SymSrvStoreFile**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[<span data-ttu-id="035b3-203">**SymSrvStoreSupplement**</span><span class="sxs-lookup"><span data-stu-id="035b3-203">**SymSrvStoreSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a><span data-ttu-id="035b3-204">Fichiers Minidump en mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="035b3-204">User-mode Minidump Files</span></span>

<span data-ttu-id="035b3-205">Les fonctions de Minidump offrent aux applications un moyen de produire des fichiers de vidage sur incident qui contiennent un sous-ensemble utile du contexte de processus entier. C’est ce qu’on appelle un [fichier Minidump](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="035b3-205">The minidump functions provide a way for applications to produce crashdump files that contain a useful subset of the entire process context; this is known as a [minidump file](minidump-files.md).</span></span> <span data-ttu-id="035b3-206">Les fonctions suivantes sont utilisées avec les fichiers minidump.</span><span class="sxs-lookup"><span data-stu-id="035b3-206">The following functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="035b3-207">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="035b3-207">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="035b3-208">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="035b3-208">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="035b3-209">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="035b3-209">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a><span data-ttu-id="035b3-210">Serveur source</span><span class="sxs-lookup"><span data-stu-id="035b3-210">Source Server</span></span>

<span data-ttu-id="035b3-211">Le [serveur source](source-server-and-source-indexing.md) permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application.</span><span class="sxs-lookup"><span data-stu-id="035b3-211">[Source server](source-server-and-source-indexing.md) enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="035b3-212">Les fonctions suivantes sont utilisées avec le serveur source.</span><span class="sxs-lookup"><span data-stu-id="035b3-212">The following functions are used with source server.</span></span>

-   [<span data-ttu-id="035b3-213">**SymGetSourceFile**</span><span class="sxs-lookup"><span data-stu-id="035b3-213">**SymGetSourceFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [<span data-ttu-id="035b3-214">**SymEnumSourceFileTokens**</span><span class="sxs-lookup"><span data-stu-id="035b3-214">**SymEnumSourceFileTokens**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [<span data-ttu-id="035b3-215">**SymEnumSourceFileTokensProc**</span><span class="sxs-lookup"><span data-stu-id="035b3-215">**SymEnumSourceFileTokensProc**</span></span>](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [<span data-ttu-id="035b3-216">**SymGetSourceFileFromToken**</span><span class="sxs-lookup"><span data-stu-id="035b3-216">**SymGetSourceFileFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [<span data-ttu-id="035b3-217">**SymGetSourceFileToken**</span><span class="sxs-lookup"><span data-stu-id="035b3-217">**SymGetSourceFileToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [<span data-ttu-id="035b3-218">**SymGetSourceVarFromToken**</span><span class="sxs-lookup"><span data-stu-id="035b3-218">**SymGetSourceVarFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a><span data-ttu-id="035b3-219">Fonctions obsolètes</span><span class="sxs-lookup"><span data-stu-id="035b3-219">Obsolete Functions</span></span>

<dl>

[<span data-ttu-id="035b3-220">**MapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="035b3-220">**MapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[<span data-ttu-id="035b3-221">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="035b3-221">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="035b3-222">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="035b3-222">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="035b3-223">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="035b3-223">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="035b3-224">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="035b3-224">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="035b3-225">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="035b3-225">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="035b3-226">**UnMapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="035b3-226">**UnMapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



