---
description: 'Étape 4 : dessiner l’image bitmap sur la zone cliente'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Étape 4 : dessiner l’image bitmap sur la zone cliente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393815"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="2dfe2-103">Étape 4 : dessiner l’image bitmap sur la zone cliente</span><span class="sxs-lookup"><span data-stu-id="2dfe2-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="2dfe2-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="2dfe2-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2dfe2-105">Cette rubrique est l’étape 4 de [saisie d’un cadre d’affiche](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="2dfe2-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="2dfe2-106">La dernière étape consiste à dessiner l’image bitmap sur la zone cliente de la fenêtre d’application, à l’aide de la fonction [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) .</span><span class="sxs-lookup"><span data-stu-id="2dfe2-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="2dfe2-107">Cet exemple peint simplement l’image bitmap dans le coin supérieur gauche de la zone cliente, sans tenir compte de la taille de la fenêtre :</span><span class="sxs-lookup"><span data-stu-id="2dfe2-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="2dfe2-108">Les variables *pbuffer* et *pbmi* sont déclarées à l' [étape 1 : créer l’infrastructure Windows](step-1--create-the-windows-framework.md)et leurs valeurs sont obtenues à [l’étape 3 : implémenter la fonction Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).</span><span class="sxs-lookup"><span data-stu-id="2dfe2-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dfe2-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2dfe2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dfe2-110">Saisie d’un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="2dfe2-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
