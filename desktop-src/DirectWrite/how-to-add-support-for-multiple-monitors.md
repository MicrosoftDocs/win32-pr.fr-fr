---
title: Comment ajouter la prise en charge de plusieurs moniteurs
description: DirectWrite prend en charge les systèmes avec plusieurs moniteurs.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382241"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Comment ajouter la prise en charge de plusieurs moniteurs

[DirectWrite](direct-write-portal.md) prend en charge les systèmes avec plusieurs moniteurs. Différentes analyses peuvent avoir une géométrie de pixels différente (RVB, BGR ou plat) ou d’autres attributs. Pour plus d’informations sur la géométrie des pixels, consultez la rubrique de référence sur la [**\_ \_ géométrie des pixels DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . Cette rubrique vous montre comment ajouter la prise en charge de plusieurs moniteurs à votre application DirectWrite.

Pour prendre en charge plusieurs analyses, vous devez gérer le message de fenêtre **WM \_ WINDOWPOSCHANGED** . Ce message est envoyé lorsque la fenêtre est déplacée. vous devez donc vérifier si la fenêtre a été déplacée vers un autre moniteur, comme illustré dans le code suivant.


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



Si la fenêtre se trouve sur une nouvelle analyse, vous devez créer des paramètres de rendu pour le nouvel analyseur à l’aide de la méthode [**IDWriteFactory :: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .

> [!Note]  
> N’utilisez pas la méthode [**IDWriteFactory :: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) pour créer les paramètres de rendu, car elle crée toujours des paramètres pour l’analyse principale.

 

Quand vous avez un objet [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , définissez les paramètres de rendu pour la cible de rendu à l’aide de la méthode [**ID2DRenderTarget :: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .

Enfin, utilisez la fonction [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) pour faire en sorte que la fenêtre redessine avec les nouveaux paramètres de rendu.

 

 