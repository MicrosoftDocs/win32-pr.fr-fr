---
description: bien que DbgHelp.dll soit fourni avec toutes les versions de Windows, les appelants doivent envisager d’utiliser l’une des versions les plus récentes de cette DLL, comme indiqué dans le package outils de débogage pour Windows. Pour plus d’informations sur la distribution de DbgHelp, consultez versions de DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Appel de la bibliothèque DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957158"
---
# <a name="calling-the-dbghelp-library"></a>Appel de la bibliothèque DbgHelp

bien que DbgHelp.dll soit fourni avec toutes les versions de Windows, les appelants doivent envisager d’utiliser l’une des versions les plus récentes de cette DLL, comme indiqué dans le package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) . Pour plus d’informations sur la distribution de DbgHelp, consultez [versions de dbghelp](dbghelp-versions.md).

quand vous utilisez DbgHelp, la meilleure stratégie consiste à installer une copie de la bibliothèque à partir du package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) dans le répertoire de l’application adjacent au logiciel qui l’appelle. Si le serveur de symboles et le serveur source sont également nécessaires, les SymSrv.dll et SrcSrv.dll doivent être installés dans le même répertoire que DbgHelp.dll, car DbgHelp appellera uniquement ces dll s’ils partagent le même répertoire avec lui. (Notez que DbgHelp n’appellera pas ces deux dll à partir du chemin de recherche standard.) Cela permet d’éviter l’utilisation de dll incompatibles ; de même, il améliore également la sécurité globale.

Le code suivant est extrait de la source de DbgHelp. Elle montre comment les versions de SymSrv.dll et de SrcSrv.dll du même répertoire que celui dans lequel DbgHelp.dll réside uniquement.


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



Après avoir chargé ces deux dll, DbgHelp appelle [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir les fonctions dont il a besoin.

Normalement, le code qui appelle DbgHelp.dll garantit que la version correcte est chargée en installant DbgHelp.dll dans le même répertoire que l’application qui a initié le processus en cours. Si le code appelant se trouve dans une DLL et n’a pas accès à l’emplacement du processus initial ou ne connaît pas celle-ci, DbgHelp.dll doit être installé en même temps que la DLL d’appel et du code similaire à celui du LoadDLL de DbgHelp doit être utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions de DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
