---
description: Le code suivant montre comment obtenir et rapporter les informations d’État détaillées à partir du gestionnaire de symboles à propos de la recherche et du chargement des modules et des fichiers de symboles correspondants.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Réception de notifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201126"
---
# <a name="getting-notifications"></a>Réception de notifications

Le code suivant montre comment obtenir et rapporter les informations d’État détaillées à partir du gestionnaire de symboles à propos de la recherche et du chargement des modules et des fichiers de symboles correspondants.

Un grand nombre d’entre eux connaissant le débogueur WinDbg peut mémoriser une commande appelée «  ! sym bruyant ». Cette commande est utilisée par l’utilisateur pour déterminer la raison pour laquelle WinDbg est ou n’est pas en mesure de charger des fichiers de symboles. Elle affiche une liste détaillée de tous les essais du gestionnaire de symboles.

Cette même liste est également disponible pour quiconque développant un client vers le gestionnaire de symboles DbgHelp.

Tout d’abord, appelez [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) avec **SYMOPT \_ Debug**. Cela amène le DbgHelp à activer les notifications de débogage.

Après l’appel de [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), utilisez [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) pour inscrire une fonction de rappel que dbghelp appellera chaque fois qu’un événement intéressant se produit. Dans cet exemple, la fonction de rappel est appelée [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback). Les fonctions de rappel de symboles sont passées à un assortiment de codes d’action qu’ils peuvent gérer en fonction du type. Dans cet exemple, nous ne prenons en charge que le code d’action de l' **\_ événement CBA** . Cette fonction passe une chaîne contenant des informations détaillées sur un événement qui s’est produit dans le processus de chargement d’un symbole. Il peut s’agir de n’importe quel événement à partir d’une tentative de lecture des données dans une image exécutable à l’emplacement de réussite d’un fichier de symboles. **SymRegisterCallbackProc64** affiche cette chaîne et retourne la **valeur true**.

> [!IMPORTANT]
> Veillez à retourner la **valeur false** à chaque code d’action que vous ne gérez pas, sinon vous risquez d’être confronté à un comportement indéfini. Reportez-vous à [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) pour obtenir la liste de tous les codes d’action et leurs implications.

 

Maintenant que le rappel est inscrit, il est temps de charger le module spécifié sur la ligne de commande en appelant [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).

Enfin, appelez [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) avant de quitter.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



La spécification de **null** comme deuxième paramètre de [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indique que le gestionnaire de symboles doit utiliser le chemin de recherche par défaut pour localiser les fichiers de symboles. Pour plus d’informations sur la façon dont le gestionnaire de symboles localise les fichiers de symboles ou sur la façon dont une application peut spécifier un chemin de recherche de symboles, consultez [chemins d'](symbol-paths.md)accès aux symboles.

L’exécution de ce programme montre comment le chemin d’accès aux symboles est traité. Au fur et à mesure que DbgHelp parcourt le chemin d’accès aux symboles pour trouver le fichier de symboles, il appelle à plusieurs reprises [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) qui, à son tour, affiche les chaînes suivantes passées par dbghelp.

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



