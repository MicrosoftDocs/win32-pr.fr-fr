---
title: Énumération de tous les modules d’un processus
description: Pour déterminer les processus qui ont chargé une DLL particulière, vous devez énumérer les modules pour chaque processus. L’exemple de code suivant utilise la fonction EnumProcessModules pour énumérer les modules des processus actuels dans le système.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315155"
---
# <a name="enumerating-all-modules-for-a-process"></a>Énumération de tous les modules d’un processus

Pour déterminer les processus qui ont chargé une DLL particulière, vous devez énumérer les modules pour chaque processus. L’exemple de code suivant utilise la fonction [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) pour énumérer les modules des processus actuels dans le système.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



La fonction principale obtient une liste de processus à l’aide de la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Pour chaque processus, la fonction main appelle la fonction PrintModules, en lui transmettant l’identificateur de processus. PrintModules appelle à son tour la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) pour obtenir le handle de processus. Si **OpenProcess** échoue, la sortie affiche uniquement l’identificateur de processus. Par exemple, **OpenProcess** échoue pour les processus inactifs et CSRSS, car leurs restrictions d’accès empêchent le code au niveau de l’utilisateur de les ouvrir. Ensuite, PrintModules appelle la fonction [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) pour obtenir la fonction handles du module. Enfin, PrintModules appelle la fonction [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) , une fois pour chaque module, pour obtenir les noms des modules.

 

 