---
title: Énumération de tous les processus
description: L’exemple de code suivant utilise la fonction EnumProcesses pour énumérer les processus actuels dans le système.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03fd9ad06bfb15924f3f5ec92d8f8858fbff60
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644111"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="26eac-103">Énumération de tous les processus</span><span class="sxs-lookup"><span data-stu-id="26eac-103">Enumerating All Processes</span></span>

<span data-ttu-id="26eac-104">L’exemple de code suivant utilise la fonction [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) pour récupérer l’identificateur de processus pour chaque objet de processus dans le système.</span><span class="sxs-lookup"><span data-stu-id="26eac-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="26eac-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) est ensuite appelé pour récupérer chaque nom de processus et l’imprimer.</span><span class="sxs-lookup"><span data-stu-id="26eac-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="26eac-106">Pour les processus 64 bits, utilisez la fonction [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .</span><span class="sxs-lookup"><span data-stu-id="26eac-106">For 64 bit processes, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="26eac-107">La fonction principale obtient une liste de processus à l’aide de la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="26eac-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="26eac-108">Pour chaque processus, main appelle la fonction **PrintProcessNameAndID** , en lui transmettant l’identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="26eac-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="26eac-109">**PrintProcessNameAndID** appelle à son tour la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) pour obtenir le handle de processus.</span><span class="sxs-lookup"><span data-stu-id="26eac-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="26eac-110">Si **OpenProcess** échoue, la sortie affiche le nom du processus sous la forme <unknown> .</span><span class="sxs-lookup"><span data-stu-id="26eac-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="26eac-111">Par exemple, **OpenProcess** échoue pour les processus inactifs et CSRSS, car leurs restrictions d’accès empêchent le code au niveau de l’utilisateur de les ouvrir.</span><span class="sxs-lookup"><span data-stu-id="26eac-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="26eac-112">Ensuite, **PrintProcessNameAndID** appelle la fonction [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) pour obtenir les descripteurs de module.</span><span class="sxs-lookup"><span data-stu-id="26eac-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="26eac-113">Enfin, **PrintProcessNameAndID** appelle la fonction [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) pour obtenir le nom du fichier exécutable et affiche le nom avec l’identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="26eac-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
