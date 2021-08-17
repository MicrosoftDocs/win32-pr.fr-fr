---
description: Lorsqu’un appel de méthode génère une erreur, de nombreuses fonctions retournent un code d’erreur.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Récupération des messages d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96ffb6627dac4f8612a80c68b1a227516ec645440c56dd7c58672cd8222c23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900506"
---
# <a name="retrieving-error-messages"></a>Récupération des messages d’erreur

Lorsqu’un appel de méthode génère une erreur, de nombreuses fonctions retournent un code d’erreur. Pour la plupart des interfaces et des éléments d’API de services de certificats qui retournent un code d’erreur, le texte du message d’erreur peut être récupéré en appelant [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) avec un handle de module **null** . Si **FormatMessage** n’aboutit pas, le code d’erreur est probablement dû à un élément API de sauvegarde ou une erreur liée à la base de données. l’appel de **FormatMessage** avec un handle de module correspondant à la bibliothèque de Ntdsbmsg.dll doit récupérer le texte du message d’erreur. L’exemple suivant montre comment récupérer le texte d’un message d’erreur dans une application de services de certificats.


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
