---
title: Récupération des erreurs réseau
description: Les fonctions WNet retournent des codes d’erreur pour la compatibilité avec Windows pour les groupes de travail. Chaque fonction WNet définit également la valeur de code d’erreur retournée par GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436d63b51d0f57698403d206774710450eee1c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510083"
---
# <a name="retrieving-network-errors"></a><span data-ttu-id="c63f4-104">Récupération des erreurs réseau</span><span class="sxs-lookup"><span data-stu-id="c63f4-104">Retrieving Network Errors</span></span>

<span data-ttu-id="c63f4-105">Les fonctions WNet retournent des codes d’erreur pour la compatibilité avec Windows pour les groupes de travail.</span><span class="sxs-lookup"><span data-stu-id="c63f4-105">The WNet functions return error codes for compatibility with Windows for Workgroups.</span></span> <span data-ttu-id="c63f4-106">Chaque fonction WNet définit également la valeur de code d’erreur retournée par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c63f4-106">Each WNet function also sets the error code value returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="c63f4-107">Quand l’une des fonctions WNet retourne une erreur \_ étendue erreur \_ , une application peut appeler la fonction [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) pour récupérer des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c63f4-107">When one of the WNet functions returns ERROR\_EXTENDED\_ERROR, an application can call the [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) function to retrieve additional information about the error.</span></span> <span data-ttu-id="c63f4-108">Ces informations sont généralement spécifiques au fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="c63f4-108">This information is usually specific to the network provider.</span></span>

<span data-ttu-id="c63f4-109">L’exemple suivant illustre une fonction de gestion des erreurs définie par l’application (NetErrorHandler).</span><span class="sxs-lookup"><span data-stu-id="c63f4-109">The following example illustrates an application-defined error-handling function (NetErrorHandler).</span></span> <span data-ttu-id="c63f4-110">La fonction accepte trois arguments : un handle de fenêtre, le code d’erreur retourné par l’une des fonctions WNet et le nom de la fonction qui a produit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c63f4-110">The function takes three arguments: a window handle, the error code returned by one of the WNet functions, and the name of the function that produced the error.</span></span> <span data-ttu-id="c63f4-111">Si le code d’erreur est erreur \_ étendue \_ d’erreur, NetErrorHandler appelle **WNetGetLastError** pour recevoir les informations d’erreur étendues et imprime les informations.</span><span class="sxs-lookup"><span data-stu-id="c63f4-111">If the error code is ERROR\_EXTENDED\_ERROR, NetErrorHandler calls **WNetGetLastError** to get extended error information and prints the information.</span></span> <span data-ttu-id="c63f4-112">L’exemple appelle la fonction [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) pour traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="c63f4-112">The sample calls the [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function to process messages.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 