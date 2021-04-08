---
description: Lorsqu’un appel de méthode génère une erreur, de nombreuses fonctions retournent un code d’erreur.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Récupération des messages d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865013"
---
# <a name="retrieving-error-messages"></a><span data-ttu-id="61bb0-103">Récupération des messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="61bb0-103">Retrieving Error Messages</span></span>

<span data-ttu-id="61bb0-104">Lorsqu’un appel de méthode génère une erreur, de nombreuses fonctions retournent un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="61bb0-104">When a method call produces an error, many functions return an error code.</span></span> <span data-ttu-id="61bb0-105">Pour la plupart des interfaces et des éléments d’API de services de certificats qui retournent un code d’erreur, le texte du message d’erreur peut être récupéré en appelant [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) avec un handle de module **null** .</span><span class="sxs-lookup"><span data-stu-id="61bb0-105">For most Certificate Services interfaces and API elements that return an error code, the error message text can be retrieved by calling [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) with a **NULL** module handle.</span></span> <span data-ttu-id="61bb0-106">Si **FormatMessage** n’aboutit pas, le code d’erreur est probablement dû à un élément API de sauvegarde ou une erreur liée à la base de données. l’appel de **FormatMessage** avec un handle de module correspondant à la bibliothèque de Ntdsbmsg.dll doit récupérer le texte du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="61bb0-106">If **FormatMessage** does not succeed, the error code most likely resulted from a backup API element or database related error; calling **FormatMessage** with a module handle corresponding to the Ntdsbmsg.dll library should retrieve the error message text.</span></span> <span data-ttu-id="61bb0-107">L’exemple suivant montre comment récupérer le texte d’un message d’erreur dans une application de services de certificats.</span><span class="sxs-lookup"><span data-stu-id="61bb0-107">The following example shows how to retrieve error message text in a Certificate Services application.</span></span>


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



 

 
