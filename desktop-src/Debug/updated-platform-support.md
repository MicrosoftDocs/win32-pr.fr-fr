---
description: Le cas échéant, la bibliothèque DbgHelp a été étendue pour prendre en charge les Windows 32 et 64 bits.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Plateforme d'appui améliorée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44389b0b46782318b3f017fe1baf8c2c0580d6993f9de4dfaa9ece64feae8c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912357"
---
# <a name="updated-platform-support"></a>Plateforme d'appui améliorée

Le cas échéant, la bibliothèque DbgHelp a été étendue pour prendre en charge les Windows 32 et 64 bits. Les définitions de fonction et de structure d’origine sont toujours dans DbgHelp. h, mais des versions mises à jour de ces définitions sont compatibles avec la Windows 64 bits. Si vous utilisez les fonctions mises à jour dans votre code, elles peuvent être compilées pour les Windows 32 et 64 bits. Votre code sera également plus efficace, car les fonctions d’origine appellent simplement les fonctions mises à jour pour effectuer le travail.

Par exemple, DbgHelp. h contient des définitions pour **SymUnloadModule** (fonction d’origine) et **SymUnloadModule64** (fonction mise à jour). Ces définitions sont presque identiques, mais utilisent des types différents pour le paramètre *BaseOfDll* . (**SymUnloadModule** utilise le type **DWORD** , tandis que **SymUnloadModule64** utilise le type **DWORD64** .) Si vous écrivez votre code pour utiliser **SymUnloadModule64**, il peut être compilé pour les Windows 32 et 64 bits. Le code est également plus efficace que s’il s’agissait d’appeler **SymUnloadModule**.

La liste suivante répertorie les fonctions mises à jour :

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

La liste suivante répertorie les structures mises à jour :

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**\_Symbole différé imagehlp \_ \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**\_SYMBOL64 en double \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**\_LINE64 imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**\_MODULE64 imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**\_SYMBOL64 imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



