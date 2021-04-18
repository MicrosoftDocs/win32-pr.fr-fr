---
description: Cette section explique comment effectuer les tâches suivantes associées aux propriétés de la fenêtre.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Utilisation des propriétés de la fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519716"
---
# <a name="using-window-properties"></a><span data-ttu-id="cb07c-103">Utilisation des propriétés de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-103">Using Window Properties</span></span>

<span data-ttu-id="cb07c-104">Cette section explique comment effectuer les tâches suivantes associées aux propriétés de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cb07c-104">This section explains how to perform the following tasks associated with window properties.</span></span>

-   [<span data-ttu-id="cb07c-105">Ajout d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-105">Adding a Window Property</span></span>](#adding-a-window-property)
-   [<span data-ttu-id="cb07c-106">Récupération d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-106">Retrieving a Window Property</span></span>](#retrieving-a-window-property)
-   [<span data-ttu-id="cb07c-107">Affichage des propriétés de fenêtre pour une fenêtre donnée</span><span class="sxs-lookup"><span data-stu-id="cb07c-107">Listing Window Properties for a Given Window</span></span>](#listing-window-properties-for-a-given-window)
-   [<span data-ttu-id="cb07c-108">Suppression d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-108">Deleting a Window Property</span></span>](#deleting-a-window-property)

## <a name="adding-a-window-property"></a><span data-ttu-id="cb07c-109">Ajout d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-109">Adding a Window Property</span></span>

<span data-ttu-id="cb07c-110">L’exemple suivant charge une icône, puis un curseur, et alloue de la mémoire pour une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cb07c-110">The following example loads an icon and then a cursor and allocates memory for a buffer.</span></span> <span data-ttu-id="cb07c-111">L’exemple utilise ensuite la fonction [**échec SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) pour assigner les descripteurs de l’icône, du curseur et de la mémoire résultants en tant que propriétés de fenêtre pour la fenêtre identifiée par la variable hwndSubclass définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="cb07c-111">The example then uses the [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) function to assign the resulting icon, cursor, and memory handles as window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="cb07c-112">Les propriétés sont identifiées par l’icône de chaîne PROP \_ , le \_ curseur prop et le tampon prop \_ .</span><span class="sxs-lookup"><span data-stu-id="cb07c-112">The properties are identified by the strings PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span>


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



## <a name="retrieving-a-window-property"></a><span data-ttu-id="cb07c-113">Récupération d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-113">Retrieving a Window Property</span></span>

<span data-ttu-id="cb07c-114">Une fenêtre peut créer des handles pour ses données de propriété de fenêtre et utiliser les données à n’importe quel motif.</span><span class="sxs-lookup"><span data-stu-id="cb07c-114">A window can create handles to its window property data and use the data for any purpose.</span></span> <span data-ttu-id="cb07c-115">L’exemple suivant utilise [**getprop**](/windows/win32/api/winuser/nf-winuser-getpropa) pour obtenir les descripteurs des propriétés de fenêtre identifiées par l' \_ icône prop, le \_ curseur PROP et le tampon prop \_ .</span><span class="sxs-lookup"><span data-stu-id="cb07c-115">The following example uses [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) to obtain handles to the window properties identified by PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span> <span data-ttu-id="cb07c-116">L’exemple affiche ensuite le contenu de la mémoire tampon, du curseur et de l’icône qui viennent d’être obtenus dans la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cb07c-116">The example then displays the contents of the newly obtained memory buffer, cursor, and icon in the window's client area.</span></span>


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



## <a name="listing-window-properties-for-a-given-window"></a><span data-ttu-id="cb07c-117">Affichage des propriétés de fenêtre pour une fenêtre donnée</span><span class="sxs-lookup"><span data-stu-id="cb07c-117">Listing Window Properties for a Given Window</span></span>

<span data-ttu-id="cb07c-118">Dans l’exemple suivant, la fonction [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) répertorie les identificateurs de chaîne des propriétés de fenêtre de la fenêtre identifiée par la variable hwndSubclass définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="cb07c-118">In the following example, the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function lists the string identifiers of the window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="cb07c-119">Cette fonction s’appuie sur la fonction de rappel définie par l’application WinPropProc pour afficher les chaînes dans la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cb07c-119">This function relies on the application-defined callback function WinPropProc to display the strings in the window's client area.</span></span>


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



## <a name="deleting-a-window-property"></a><span data-ttu-id="cb07c-120">Suppression d’une propriété de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cb07c-120">Deleting a Window Property</span></span>

<span data-ttu-id="cb07c-121">Quand une fenêtre est détruite, elle doit détruire toutes les propriétés de fenêtre qu’elle a définies.</span><span class="sxs-lookup"><span data-stu-id="cb07c-121">When a window is destroyed, it must destroy any window properties it set.</span></span> <span data-ttu-id="cb07c-122">L’exemple suivant utilise la fonction [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) et la fonction de rappel définie par l’application DelPropProc pour détruire les propriétés associées à la fenêtre identifiée par la variable hwndSubclass définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="cb07c-122">The following example uses the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function and the application-defined callback function DelPropProc to destroy the properties associated with the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="cb07c-123">La fonction de rappel, qui utilise la fonction [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) , est également affichée.</span><span class="sxs-lookup"><span data-stu-id="cb07c-123">The callback function, which uses the [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) function, is also shown.</span></span>


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



 

 
