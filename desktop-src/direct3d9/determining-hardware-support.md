---
description: Direct3D fournit les fonctions suivantes pour déterminer la prise en charge matérielle.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Détermination de la prise en charge matérielle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516742"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="274a7-103">Détermination de la prise en charge matérielle (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="274a7-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="274a7-104">Direct3D fournit les fonctions suivantes pour déterminer la prise en charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="274a7-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="274a7-105">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="274a7-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="274a7-106">Permet de vérifier si un format de surface peut être utilisé comme texture, si un format de surface peut être utilisé comme texture et une cible de rendu, ou si un format de surface peut être utilisé comme tampon de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="274a7-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="274a7-107">De plus, cette méthode est utilisée pour vérifier la prise en charge du format de mémoire tampon de profondeur et la prise en charge du format de tampon de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="274a7-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="274a7-108">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="274a7-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="274a7-109">Permet de vérifier la capacité d’un appareil à effectuer une accélération matérielle, la capacité d’un appareil à créer une chaîne de permutation à des fins de présentation ou la capacité d’un appareil à effectuer un rendu au format d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="274a7-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="274a7-110">**IDirect3D9::CheckDepthStencilMatch**</span><span class="sxs-lookup"><span data-stu-id="274a7-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="274a7-111">Permet de vérifier si un format de mémoire tampon de stencil de profondeur est compatible avec un format de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="274a7-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="274a7-112">Notez qu’avant d’appeler cette méthode, l’application doit appeler [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sur les formats de stencil de profondeur et de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="274a7-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="274a7-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="274a7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="274a7-114">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="274a7-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
