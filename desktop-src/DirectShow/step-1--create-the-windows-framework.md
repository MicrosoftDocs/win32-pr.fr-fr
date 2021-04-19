---
description: 'Étape 1 : créer le Framework Windows'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Étape 1 : créer le Framework Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538909"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="e086a-103">Étape 1 : créer le Framework Windows</span><span class="sxs-lookup"><span data-stu-id="e086a-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="e086a-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="e086a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e086a-105">Commencez par créer la structure de base d’une application Windows, y compris WinMain et une procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e086a-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="e086a-106">La fonction WinMain n’est pas illustrée ici ; Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) avant la boucle de message pour initialiser la bibliothèque com et [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) après la sortie de la boucle de message.</span><span class="sxs-lookup"><span data-stu-id="e086a-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="e086a-107">Démarrez avec la procédure de fenêtre minimale suivante :</span><span class="sxs-lookup"><span data-stu-id="e086a-107">Start with the following minimal window procedure:</span></span>


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



<span data-ttu-id="e086a-108">Lorsque vous récupérez une image postérisée à partir du détecteur de média, elle retourne une mémoire tampon qui contient une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) suivie des bits d’image.</span><span class="sxs-lookup"><span data-stu-id="e086a-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="e086a-109">Par conséquent, définissez deux variables statiques dans la procédure de fenêtre : *pbmi* contiendra un pointeur vers la structure **BITMAPINFOHEADER** , et *pbuffer* contiendra un pointeur vers l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="e086a-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="e086a-110">L’application alloue la mémoire tampon dans *pbmi* à l’aide de `new` , donc elle doit supprimer la mémoire tampon avant la destruction de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e086a-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="e086a-111">Le pointeur *pbuffer* est calculé comme un décalage par rapport à *pbmi*. il n’est donc pas nécessaire de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="e086a-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="e086a-112">Suivant : [étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="e086a-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e086a-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e086a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e086a-114">Saisie d’un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="e086a-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
