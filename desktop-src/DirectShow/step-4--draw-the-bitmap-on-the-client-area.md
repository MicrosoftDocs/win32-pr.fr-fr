---
description: 'Étape 4 : dessiner l’image bitmap sur la zone cliente'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Étape 4 : dessiner l’image bitmap sur la zone cliente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253e7d8a5b7508d5ae9f27195dbb7d59b30508ff2aacd8ec2713e0f4d6c909f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951788"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Étape 4 : dessiner l’image bitmap sur la zone cliente

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cette rubrique est l’étape 4 de [saisie d’un cadre d’affiche](grabbing-a-poster-frame.md).

La dernière étape consiste à dessiner l’image bitmap sur la zone cliente de la fenêtre d’application, à l’aide de la fonction [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) . Cet exemple peint simplement l’image bitmap dans le coin supérieur gauche de la zone cliente, sans tenir compte de la taille de la fenêtre :


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



les variables *pBuffer* et *pbmi* sont déclarées à l' [étape 1 : créer le Windows Framework](step-1--create-the-windows-framework.md), et leurs valeurs sont obtenues à [l’étape 3 : implémenter la fonction Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Saisie d’un cadre d’affiche](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
