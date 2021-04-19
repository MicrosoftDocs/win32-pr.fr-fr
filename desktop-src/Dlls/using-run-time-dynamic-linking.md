---
description: Vous pouvez utiliser la même DLL dans la liaison dynamique au moment du chargement et au moment de l’exécution.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Utilisation de la liaison dynamique Run-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524573"
---
# <a name="using-run-time-dynamic-linking"></a><span data-ttu-id="1d910-103">Utilisation de la liaison dynamique Run-Time</span><span class="sxs-lookup"><span data-stu-id="1d910-103">Using Run-Time Dynamic Linking</span></span>

<span data-ttu-id="1d910-104">Vous pouvez utiliser la même DLL dans la liaison dynamique au moment du chargement et au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1d910-104">You can use the same DLL in both load-time and run-time dynamic linking.</span></span> <span data-ttu-id="1d910-105">L’exemple suivant utilise la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour obtenir un handle vers la dll Myputs (consultez [création d’une bibliothèque de Dynamic-Link simple](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="1d910-105">The following example uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to get a handle to the Myputs DLL (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span> <span data-ttu-id="1d910-106">Si **LoadLibrary** parvient à fonctionner, le programme utilise le handle retourné dans la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse de la fonction myPuts de la dll.</span><span class="sxs-lookup"><span data-stu-id="1d910-106">If **LoadLibrary** succeeds, the program uses the returned handle in the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of the DLL's myPuts function.</span></span> <span data-ttu-id="1d910-107">Après l’appel de la fonction DLL, le programme appelle la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) pour décharger la dll.</span><span class="sxs-lookup"><span data-stu-id="1d910-107">After calling the DLL function, the program calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function to unload the DLL.</span></span>

<span data-ttu-id="1d910-108">Étant donné que le programme utilise la liaison dynamique au moment de l’exécution, il n’est pas nécessaire de lier le module à une bibliothèque d’importation pour la DLL.</span><span class="sxs-lookup"><span data-stu-id="1d910-108">Because the program uses run-time dynamic linking, it is not necessary to link the module with an import library for the DLL.</span></span>

<span data-ttu-id="1d910-109">Cet exemple illustre une différence importante entre la liaison dynamique au moment de l’exécution et au moment du chargement.</span><span class="sxs-lookup"><span data-stu-id="1d910-109">This example illustrates an important difference between run-time and load-time dynamic linking.</span></span> <span data-ttu-id="1d910-110">Si la DLL n’est pas disponible, l’application qui utilise la liaison dynamique au moment du chargement doit se terminer simplement.</span><span class="sxs-lookup"><span data-stu-id="1d910-110">If the DLL is not available, the application using load-time dynamic linking must simply terminate.</span></span> <span data-ttu-id="1d910-111">Toutefois, l’exemple de liaison dynamique au moment de l’exécution peut répondre à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1d910-111">The run-time dynamic linking example, however, can respond to the error.</span></span>


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a><span data-ttu-id="1d910-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d910-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d910-113">Liaison dynamique au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="1d910-113">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
</dt> </dl>

 

 
