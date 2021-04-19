---
title: Recherche de texte pour les numéros de code d’erreur
description: Il est parfois nécessaire d’afficher le texte d’erreur associé aux codes d’erreur renvoyés par les fonctions liées au réseau. Vous devrez peut-être effectuer cette tâche avec les fonctions de gestion de réseau fournies par le système.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513722"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Recherche de texte pour les numéros de code d’erreur

Il est parfois nécessaire d’afficher le texte d’erreur associé aux codes d’erreur renvoyés par les fonctions liées au réseau. Vous devrez peut-être effectuer cette tâche avec les fonctions de gestion de réseau fournies par le système.

Le texte d’erreur pour ces messages se trouve dans le fichier de table de messages nommé Netmsg.dll, qui se trouve dans% SystemRoot% \\ system32. Ce fichier contient des messages d’erreur dans la plage NERR \_ (2100) au maximum de \_ NERR (NERR \_ base + 899). Ces codes d’erreur sont définis dans le fichier d’en-tête du kit de développement logiciel lmerr. h.

Les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) peuvent charger des Netmsg.dll. La fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) mappe un code d’erreur au texte du message, étant donné un handle de module au fichier Netmsg.dll.

L’exemple suivant montre comment afficher le texte d’erreur associé aux fonctions de gestion de réseau, en plus de l’affichage du texte d’erreur associé aux codes d’erreur liés au système. Si le numéro d’erreur fourni se trouve dans une plage spécifique, le module de message netmsg.dll est chargé et utilisé pour rechercher le numéro d’erreur spécifié avec la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



Après avoir compilé ce programme, vous pouvez insérer le numéro de code d’erreur comme argument et le programme affichera le texte. Par exemple :

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 