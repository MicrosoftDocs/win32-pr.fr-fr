---
title: Comment créer une chaîne de permutation
description: Cette rubrique montre comment créer une chaîne de permutation qui encapsule au moins deux mémoires tampons utilisées pour le rendu et l’affichage.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382289"
---
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="f4e79-103">Comment : créer une chaîne de permutation</span><span class="sxs-lookup"><span data-stu-id="f4e79-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="f4e79-104">Cette rubrique montre comment créer une chaîne de permutation qui encapsule au moins deux mémoires tampons utilisées pour le rendu et l’affichage.</span><span class="sxs-lookup"><span data-stu-id="f4e79-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="f4e79-105">Ils contiennent généralement un tampon d’avant présenté au périphérique d’affichage et une mémoire tampon d’arrière-plan qui sert de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="f4e79-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="f4e79-106">Une fois le contexte immédiat rendu sur la mémoire tampon d’arrière-plan, la chaîne de permutation présente la mémoire tampon d’arrière-plan en échangeant les deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="f4e79-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="f4e79-107">La chaîne de permutation définit plusieurs caractéristiques de rendu, notamment :</span><span class="sxs-lookup"><span data-stu-id="f4e79-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="f4e79-108">Taille de la zone de rendu.</span><span class="sxs-lookup"><span data-stu-id="f4e79-108">The size of the render area.</span></span>
-   <span data-ttu-id="f4e79-109">Fréquence d’actualisation de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="f4e79-109">The display refresh rate.</span></span>
-   <span data-ttu-id="f4e79-110">Mode d'affichage.</span><span class="sxs-lookup"><span data-stu-id="f4e79-110">The display mode.</span></span>
-   <span data-ttu-id="f4e79-111">Format de surface.</span><span class="sxs-lookup"><span data-stu-id="f4e79-111">The surface format.</span></span>

<span data-ttu-id="f4e79-112">Définissez les caractéristiques de la chaîne de permutation en remplissant une structure [**desc de \_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) et en initialisant une interface [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) .</span><span class="sxs-lookup"><span data-stu-id="f4e79-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="f4e79-113">Initialisez une chaîne de permutation en appelant [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="f4e79-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="f4e79-114">Créer un appareil et une chaîne de permutation</span><span class="sxs-lookup"><span data-stu-id="f4e79-114">Create a device and a swap chain</span></span>

<span data-ttu-id="f4e79-115">Pour initialiser un appareil et une chaîne de permutation, utilisez l’une des deux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4e79-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="f4e79-116">Utilisez la fonction [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) lorsque vous souhaitez initialiser la chaîne de permutation en même temps que l’initialisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4e79-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="f4e79-117">Il s’agit généralement de l’option la plus simple.</span><span class="sxs-lookup"><span data-stu-id="f4e79-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="f4e79-118">Utilisez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) lorsque vous avez déjà créé une chaîne de permutation à l’aide de [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span><span class="sxs-lookup"><span data-stu-id="f4e79-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4e79-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4e79-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e79-120">Appareils</span><span class="sxs-lookup"><span data-stu-id="f4e79-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="f4e79-121">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="f4e79-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 