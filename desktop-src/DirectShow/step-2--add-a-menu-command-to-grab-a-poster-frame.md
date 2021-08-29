---
description: 'Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282ba112a9035edd9e75c9ea28709ec9c5dc137562ec75dbc5121de04dad864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650899"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cette rubrique est l’étape 2 de [la saisie d’un cadre d’affiche](grabbing-a-poster-frame.md).

Ensuite, ajoutez une commande pour que l’utilisateur récupère un cadre d’affiche à partir d’un fichier. Créez un élément de menu avec l’ID de ressource de la \_ bitmap IDM, puis ajoutez l’instruction case suivante à la procédure de fenêtre :


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



La fonction DoShowBitmap retourne la mémoire tampon allouée dans *pbmi*. En supposant que la fonction aboutisse, l’adresse de la bitmap (


```C++
pBuffer
```



) peut être calculé en tant que décalage à partir de *pbmi*. Dans la fonction DoShowBitmap, affichez une boîte de dialogue **ouvrir un fichier** permettant à l’utilisateur de choisir un fichier, puis appelez la fonction GetBitmap définie par l’application, qui récupérera l’image bitmap :


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



[Étape 3 : implémenter la fonction Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Saisie d’un cadre d’affiche](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



