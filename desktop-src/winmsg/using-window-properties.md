---
description: Cette section explique comment effectuer les tâches suivantes associées aux propriétés de la fenêtre.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Utilisation des propriétés de la fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fcb4cb0346554ee2df5c1b2fc92df7675cd61d11799b891156b13f26fb213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028267"
---
# <a name="using-window-properties"></a>Utilisation des propriétés de la fenêtre

Cette section explique comment effectuer les tâches suivantes associées aux propriétés de la fenêtre.

-   [Ajout d’une propriété de fenêtre](#adding-a-window-property)
-   [Récupération d’une propriété de fenêtre](#retrieving-a-window-property)
-   [Affichage des propriétés de fenêtre pour une fenêtre donnée](#listing-window-properties-for-a-given-window)
-   [Suppression d’une propriété de fenêtre](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Ajout d’une propriété de fenêtre

L’exemple suivant charge une icône, puis un curseur, et alloue de la mémoire pour une mémoire tampon. L’exemple utilise ensuite la fonction [**échec SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) pour assigner les descripteurs de l’icône, du curseur et de la mémoire résultants en tant que propriétés de fenêtre pour la fenêtre identifiée par la variable hwndSubclass définie par l’application. Les propriétés sont identifiées par l’icône de chaîne PROP \_ , le \_ curseur prop et le tampon prop \_ .


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>Récupération d’une propriété de fenêtre

Une fenêtre peut créer des handles pour ses données de propriété de fenêtre et utiliser les données à n’importe quel motif. L’exemple suivant utilise [**getprop**](/windows/win32/api/winuser/nf-winuser-getpropa) pour obtenir les descripteurs des propriétés de fenêtre identifiées par l' \_ icône prop, le \_ curseur PROP et le tampon prop \_ . L’exemple affiche ensuite le contenu de la mémoire tampon, du curseur et de l’icône qui viennent d’être obtenus dans la zone cliente de la fenêtre.


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>Affichage des propriétés de fenêtre pour une fenêtre donnée

Dans l’exemple suivant, la fonction [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) répertorie les identificateurs de chaîne des propriétés de fenêtre de la fenêtre identifiée par la variable hwndSubclass définie par l’application. Cette fonction s’appuie sur la fonction de rappel définie par l’application WinPropProc pour afficher les chaînes dans la zone cliente de la fenêtre.


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>Suppression d’une propriété de fenêtre

Quand une fenêtre est détruite, elle doit détruire toutes les propriétés de fenêtre qu’elle a définies. L’exemple suivant utilise la fonction [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) et la fonction de rappel définie par l’application DelPropProc pour détruire les propriétés associées à la fenêtre identifiée par la variable hwndSubclass définie par l’application. La fonction de rappel, qui utilise la fonction [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) , est également affichée.


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
