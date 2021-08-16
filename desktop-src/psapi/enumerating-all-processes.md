---
title: Énumération de tous les processus
description: L’exemple de code suivant utilise la fonction EnumProcesses pour énumérer les processus actuels dans le système.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89798ed3d2d7e44f014d95833302edb5d5be078daf557eed32d3496c863539e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681006"
---
# <a name="enumerating-all-processes"></a>Énumération de tous les processus

L’exemple de code suivant utilise la fonction [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) pour récupérer l’identificateur de processus pour chaque objet de processus dans le système. [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) est ensuite appelé pour récupérer chaque nom de processus et l’imprimer.

>[!NOTE]
> Pour les processus 64 bits, utilisez la fonction [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .

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



La fonction principale obtient une liste de processus à l’aide de la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Pour chaque processus, main appelle la fonction **PrintProcessNameAndID** , en lui transmettant l’identificateur de processus. **PrintProcessNameAndID** appelle à son tour la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) pour obtenir le handle de processus. Si **OpenProcess** échoue, la sortie affiche le nom du processus sous la forme <unknown> . Par exemple, **OpenProcess** échoue pour les processus inactifs et CSRSS, car leurs restrictions d’accès empêchent le code au niveau de l’utilisateur de les ouvrir. Ensuite, **PrintProcessNameAndID** appelle la fonction [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) pour obtenir les descripteurs de module. Enfin, **PrintProcessNameAndID** appelle la fonction [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) pour obtenir le nom du fichier exécutable et affiche le nom avec l’identificateur de processus.

 

 
