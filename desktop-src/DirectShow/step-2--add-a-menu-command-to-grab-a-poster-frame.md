---
description: 'Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115774"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="067ef-103">Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="067ef-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="067ef-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="067ef-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="067ef-105">Cette rubrique est l’étape 2 de [la saisie d’un cadre d’affiche](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="067ef-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="067ef-106">Ensuite, ajoutez une commande pour que l’utilisateur récupère un cadre d’affiche à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="067ef-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="067ef-107">Créez un élément de menu avec l’ID de ressource de la \_ bitmap IDM, puis ajoutez l’instruction case suivante à la procédure de fenêtre :</span><span class="sxs-lookup"><span data-stu-id="067ef-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



<span data-ttu-id="067ef-108">La fonction DoShowBitmap retourne la mémoire tampon allouée dans *pbmi*.</span><span class="sxs-lookup"><span data-stu-id="067ef-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="067ef-109">En supposant que la fonction aboutisse, l’adresse de la bitmap (</span><span class="sxs-lookup"><span data-stu-id="067ef-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="067ef-110">) peut être calculé en tant que décalage à partir de *pbmi*.</span><span class="sxs-lookup"><span data-stu-id="067ef-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="067ef-111">Dans la fonction DoShowBitmap, affichez une boîte de dialogue **ouvrir un fichier** permettant à l’utilisateur de choisir un fichier, puis appelez la fonction GetBitmap définie par l’application, qui récupérera l’image bitmap :</span><span class="sxs-lookup"><span data-stu-id="067ef-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



<span data-ttu-id="067ef-112">[Étape 3 : implémenter la fonction Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)</span><span class="sxs-lookup"><span data-stu-id="067ef-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="067ef-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="067ef-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="067ef-114">Saisie d’un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="067ef-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



