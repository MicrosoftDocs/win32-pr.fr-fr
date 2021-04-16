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
# <a name="dbghelp-functions"></a>Fonctions DbgHelp

Voici les fonctions DbgHelp.

## <a name="general"></a>Général

Les fonctions d’assistance générales sont les suivantes :

<dl>

[**EnumDirTree**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[**ImagehlpApiVersion**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[**ImagehlpApiVersionEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[**MakeSureDirectoryPathExists**](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[**SearchTreeForFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a>Débogueur

Les fonctions de service de débogage sont les fonctions les plus adaptées à une utilisation par un débogueur ou le code de débogage dans une application. Ces fonctions peuvent être utilisées conjointement avec les fonctions de gestionnaire de symboles pour une utilisation plus facile.

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**EnumerateLoadedModulesEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[**FindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[**FindDebugInfoFileEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[**FindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[**FindExecutableImageEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymSetParentWindow**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a>Accès aux images

Les fonctions d’accès à l’image accèdent aux données d’une image exécutable. Les fonctions fournissent un accès de haut niveau à la base d’images et un accès très spécifique aux parties les plus courantes des données d’une image.

<dl>

[**GetTimestampForLoadedLibrary**](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[**Échec imagedirectoryentrytodata**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[**ImageDirectoryEntryToDataEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[**ImageNtHeader**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[**ImageRvaToSection**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[**ImageRvaToVa**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a>Gestionnaire de symboles

Les fonctions de [Gestionnaire de symboles](symbol-handling.md) offrent aux applications un accès facile et portable aux informations de débogage symboliques d’une image. Ces fonctions doivent être utilisées exclusivement pour garantir l’accès aux informations symboliques. Cela est nécessaire, car ces fonctions isolent l’application du format des symboles.

<dl>

[**SymAddSourceStream**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[**SymAddSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[**SymDeleteSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumLines**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[**SymEnumProcesses**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[**SymEnumSourceLines**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[**SymEnumSymbolsForAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[**SymEnumTypes**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[**SymEnumTypesByName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[**SymFindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[**SymFindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[**SymFindFileInPath**](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[**SymFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[**SymFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetFileLineOffsets64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[**SymGetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetOmaps**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[**SymGetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[**SymGetScope**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[**SymGetSymbolFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[**SymGetTypeFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[**SymGetTypeInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[**SymGetTypeInfoEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[**SymMatchFileName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[**SymMatchString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[**SymNext**](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[**SymPrev**](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymSearch**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[**SymSetScopeFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[**SymSetScopeFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a>Serveur de symboles

Le [serveur de symboles](symbol-servers-and-symbol-stores.md) permet aux débogueurs de récupérer automatiquement les fichiers de symboles appropriés sans les noms de produits, les mises en production ou les numéros de Build. Les fonctions suivantes sont utilisées avec le serveur de symboles.

<dl>

[**SymSrvDeltaName**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[**SymSrvGetFileIndexes**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[**SymSrvGetFileIndexInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[**SymSrvGetFileIndexString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[**SymSrvGetSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[**SymSrvIsStore**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[**SymSrvStoreFile**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[**SymSrvStoreSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a>Fichiers Minidump en mode utilisateur

Les fonctions de Minidump offrent aux applications un moyen de produire des fichiers de vidage sur incident qui contiennent un sous-ensemble utile du contexte de processus entier. C’est ce qu’on appelle un [fichier Minidump](minidump-files.md). Les fonctions suivantes sont utilisées avec les fichiers minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**Entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a>Serveur source

Le [serveur source](source-server-and-source-indexing.md) permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application. Les fonctions suivantes sont utilisées avec le serveur source.

-   [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [**SymEnumSourceFileTokens**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [**SymEnumSourceFileTokensProc**](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [**SymGetSourceFileFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [**SymGetSourceFileToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [**SymGetSourceVarFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a>Fonctions obsolètes

<dl>

[**MapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**UnMapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



