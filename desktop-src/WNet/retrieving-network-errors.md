---
title: Récupération des erreurs réseau
description: les fonctions WNet retournent des codes d’erreur pour la compatibilité avec Windows pour les groupes de travail. Chaque fonction WNet définit également la valeur de code d’erreur retournée par GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f02a05ab93d50b9c448ae280e5de7ddbed1260cf1df8b8b3e56aa33aaeff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072019"
---
# <a name="retrieving-network-errors"></a>Récupération des erreurs réseau

les fonctions WNet retournent des codes d’erreur pour la compatibilité avec Windows pour les groupes de travail. Chaque fonction WNet définit également la valeur de code d’erreur retournée par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Quand l’une des fonctions WNet retourne une erreur \_ étendue erreur \_ , une application peut appeler la fonction [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) pour récupérer des informations supplémentaires sur l’erreur. Ces informations sont généralement spécifiques au fournisseur réseau.

L’exemple suivant illustre une fonction de gestion des erreurs définie par l’application (NetErrorHandler). La fonction accepte trois arguments : un handle de fenêtre, le code d’erreur retourné par l’une des fonctions WNet et le nom de la fonction qui a produit l’erreur. Si le code d’erreur est erreur \_ étendue \_ d’erreur, NetErrorHandler appelle **WNetGetLastError** pour recevoir les informations d’erreur étendues et imprime les informations. L’exemple appelle la fonction [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) pour traiter les messages.


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



 

 