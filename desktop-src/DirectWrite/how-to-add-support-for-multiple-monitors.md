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
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="03196-103">Comment ajouter la prise en charge de plusieurs moniteurs</span><span class="sxs-lookup"><span data-stu-id="03196-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="03196-104">[DirectWrite](direct-write-portal.md) prend en charge les systèmes avec plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="03196-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="03196-105">Différentes analyses peuvent avoir une géométrie de pixels différente (RVB, BGR ou plat) ou d’autres attributs.</span><span class="sxs-lookup"><span data-stu-id="03196-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="03196-106">Pour plus d’informations sur la géométrie des pixels, consultez la rubrique de référence sur la [**\_ \_ géométrie des pixels DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) .</span><span class="sxs-lookup"><span data-stu-id="03196-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="03196-107">Cette rubrique vous montre comment ajouter la prise en charge de plusieurs moniteurs à votre application DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="03196-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="03196-108">Pour prendre en charge plusieurs analyses, vous devez gérer le message de fenêtre **WM \_ WINDOWPOSCHANGED** .</span><span class="sxs-lookup"><span data-stu-id="03196-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="03196-109">Ce message est envoyé lorsque la fenêtre est déplacée. vous devez donc vérifier si la fenêtre a été déplacée vers un autre moniteur, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="03196-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


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



<span data-ttu-id="03196-110">Si la fenêtre se trouve sur une nouvelle analyse, vous devez créer des paramètres de rendu pour le nouvel analyseur à l’aide de la méthode [**IDWriteFactory :: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="03196-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="03196-111">N’utilisez pas la méthode [**IDWriteFactory :: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) pour créer les paramètres de rendu, car elle crée toujours des paramètres pour l’analyse principale.</span><span class="sxs-lookup"><span data-stu-id="03196-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="03196-112">Quand vous avez un objet [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , définissez les paramètres de rendu pour la cible de rendu à l’aide de la méthode [**ID2DRenderTarget :: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="03196-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="03196-113">Enfin, utilisez la fonction [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) pour faire en sorte que la fenêtre redessine avec les nouveaux paramètres de rendu.</span><span class="sxs-lookup"><span data-stu-id="03196-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 