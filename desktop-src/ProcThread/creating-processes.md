---
description: La fonction CreateProcess crée un nouveau processus, qui s’exécute indépendamment du processus de création. Toutefois, pour plus de simplicité, la relation est appelée relation parent-enfant.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Création de processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951978"
---
# <a name="creating-processes"></a>Création de processus

La fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crée un nouveau processus, qui s’exécute indépendamment du processus de création. Toutefois, pour plus de simplicité, la relation est appelée relation parent-enfant.

Le code suivant montre comment créer un processus.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



Si [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) parvient à fonctionner, elle retourne une structure d' [**\_ informations de processus**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) contenant des handles et des identificateurs pour le nouveau processus et son thread principal. Les handles de thread et de processus sont créés avec des droits d’accès complets, même si l’accès peut être restreint si vous spécifiez des descripteurs de sécurité. Lorsque vous n’avez plus besoin de ces handles, fermez-les à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Vous pouvez également créer un processus à l’aide de la fonction [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) . Cela vous permet de spécifier le contexte de sécurité du compte d’utilisateur dans lequel le processus s’exécutera.

 

 
