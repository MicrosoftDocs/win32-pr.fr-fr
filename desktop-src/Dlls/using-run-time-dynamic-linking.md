---
description: Vous pouvez utiliser la même DLL dans la liaison dynamique au moment du chargement et au moment de l’exécution.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Utilisation de la liaison dynamique Run-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255979"
---
# <a name="using-run-time-dynamic-linking"></a>Utilisation de la liaison dynamique Run-Time

Vous pouvez utiliser la même DLL dans la liaison dynamique au moment du chargement et au moment de l’exécution. L’exemple suivant utilise la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour obtenir un handle vers la dll Myputs (consultez [création d’une bibliothèque de Dynamic-Link simple](creating-a-simple-dynamic-link-library.md)). Si **LoadLibrary** parvient à fonctionner, le programme utilise le handle retourné dans la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse de la fonction myPuts de la dll. Après l’appel de la fonction DLL, le programme appelle la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) pour décharger la dll.

Étant donné que le programme utilise la liaison dynamique au moment de l’exécution, il n’est pas nécessaire de lier le module à une bibliothèque d’importation pour la DLL.

Cet exemple illustre une différence importante entre la liaison dynamique au moment de l’exécution et au moment du chargement. Si la DLL n’est pas disponible, l’application qui utilise la liaison dynamique au moment du chargement doit se terminer simplement. Toutefois, l’exemple de liaison dynamique au moment de l’exécution peut répondre à l’erreur.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison dynamique au moment de l’exécution](run-time-dynamic-linking.md)
</dt> </dl>

 

 
