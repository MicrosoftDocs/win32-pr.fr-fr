---
description: 'étape 1 : créer le Framework Windows'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'étape 1 : créer le Framework Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feba710c8df948e34c0da0ca9e7a1de85622bfae462290cbce3f36777854cb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072513"
---
# <a name="step-1-create-the-windows-framework"></a>étape 1 : créer le Framework Windows

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

commencez par créer la structure de base d’une application Windows, y compris WinMain et une procédure de fenêtre. La fonction WinMain n’est pas illustrée ici ; Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) avant la boucle de message pour initialiser la bibliothèque com et [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) après la sortie de la boucle de message. Démarrez avec la procédure de fenêtre minimale suivante :


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



Lorsque vous récupérez une image postérisée à partir du détecteur de média, elle retourne une mémoire tampon qui contient une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) suivie des bits d’image. Par conséquent, définissez deux variables statiques dans la procédure de fenêtre : *pbmi* contiendra un pointeur vers la structure **BITMAPINFOHEADER** , et *pbuffer* contiendra un pointeur vers l’image bitmap. L’application alloue la mémoire tampon dans *pbmi* à l’aide de `new` , donc elle doit supprimer la mémoire tampon avant la destruction de la fenêtre. Le pointeur *pbuffer* est calculé comme un décalage par rapport à *pbmi*. il n’est donc pas nécessaire de le supprimer.

Suivant : [étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Saisie d’un cadre d’affiche](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
