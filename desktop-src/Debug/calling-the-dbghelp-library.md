---
description: Bien que DbgHelp.dll soit fourni avec toutes les versions de Windows, les appelants doivent envisager d’utiliser l’une des versions les plus récentes de cette DLL, comme indiqué dans le package outils de débogage pour Windows. Pour plus d’informations sur la distribution de DbgHelp, consultez versions de DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Appel de la bibliothèque DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482752"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="26c29-104">Appel de la bibliothèque DbgHelp</span><span class="sxs-lookup"><span data-stu-id="26c29-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="26c29-105">Bien que DbgHelp.dll soit fourni avec toutes les versions de Windows, les appelants doivent envisager d’utiliser l’une des versions les plus récentes de cette DLL, comme indiqué dans le package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="26c29-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="26c29-106">Pour plus d’informations sur la distribution de DbgHelp, consultez [versions de dbghelp](dbghelp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="26c29-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="26c29-107">Lors de l’utilisation de DbgHelp, la meilleure stratégie consiste à installer une copie de la bibliothèque à partir du package [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) dans le répertoire de l’application, qui est logiquement adjacent au logiciel qui l’appelle.</span><span class="sxs-lookup"><span data-stu-id="26c29-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="26c29-108">Si le serveur de symboles et le serveur source sont également nécessaires, les SymSrv.dll et SrcSrv.dll doivent être installés dans le même répertoire que DbgHelp.dll, car DbgHelp appellera uniquement ces dll s’ils partagent le même répertoire avec lui.</span><span class="sxs-lookup"><span data-stu-id="26c29-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="26c29-109">(Notez que DbgHelp n’appellera pas ces deux dll à partir du chemin de recherche standard.) Cela permet d’éviter l’utilisation de dll incompatibles ; de même, il améliore également la sécurité globale.</span><span class="sxs-lookup"><span data-stu-id="26c29-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="26c29-110">Le code suivant est extrait de la source de DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="26c29-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="26c29-111">Elle montre comment les versions de SymSrv.dll et de SrcSrv.dll du même répertoire que celui dans lequel DbgHelp.dll réside uniquement.</span><span class="sxs-lookup"><span data-stu-id="26c29-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


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



<span data-ttu-id="26c29-112">Après avoir chargé ces deux dll, DbgHelp appelle [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir les fonctions dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="26c29-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="26c29-113">Normalement, le code qui appelle DbgHelp.dll garantit que la version correcte est chargée en installant DbgHelp.dll dans le même répertoire que l’application qui a initié le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="26c29-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="26c29-114">Si le code appelant se trouve dans une DLL et n’a pas accès à l’emplacement du processus initial ou ne connaît pas celle-ci, DbgHelp.dll doit être installé en même temps que la DLL d’appel et du code similaire à celui du LoadDLL de DbgHelp doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="26c29-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26c29-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26c29-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26c29-116">Versions de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="26c29-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="26c29-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="26c29-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="26c29-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="26c29-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="26c29-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="26c29-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
