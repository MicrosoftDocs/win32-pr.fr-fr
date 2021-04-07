---
description: Une surface représente une zone linéaire de la mémoire d’affichage et se trouve généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système. Les surfaces sont gérées par l’interface IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Surfaces Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745397"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="16b89-104">Surfaces Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="16b89-105">Une surface représente une zone linéaire de la mémoire d’affichage et se trouve généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="16b89-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="16b89-106">Les surfaces sont gérées par l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="16b89-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="16b89-107">Mémoire tampon d’avant.</span><span class="sxs-lookup"><span data-stu-id="16b89-107">Front Buffer.</span></span> <span data-ttu-id="16b89-108">Rectangle de mémoire qui est traduit par la carte graphique et affiché sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="16b89-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="16b89-109">Dans Direct3D, une application n’écrit jamais directement dans le tampon d’avant.</span><span class="sxs-lookup"><span data-stu-id="16b89-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="16b89-110">Mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="16b89-110">Back Buffer.</span></span> <span data-ttu-id="16b89-111">Rectangle de mémoire dans lequel une application peut écrire directement.</span><span class="sxs-lookup"><span data-stu-id="16b89-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="16b89-112">La mémoire tampon d’arrière-plan n’est jamais directement affichée sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="16b89-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="16b89-113">Retournement des surfaces.</span><span class="sxs-lookup"><span data-stu-id="16b89-113">Flipping surfaces.</span></span> <span data-ttu-id="16b89-114">Processus de déplacement de la mémoire tampon d’arrière-plan vers la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="16b89-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="16b89-115">Chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="16b89-115">Swap chain.</span></span> <span data-ttu-id="16b89-116">Collection d’une ou plusieurs mémoires tampons d’arrière-plan qui peuvent être présentées en série au tampon d’avant.</span><span class="sxs-lookup"><span data-stu-id="16b89-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="16b89-117">Obtention d’une surface</span><span class="sxs-lookup"><span data-stu-id="16b89-117">Getting a Surface</span></span>

<span data-ttu-id="16b89-118">Créez une surface en appelant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="16b89-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="16b89-119">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="16b89-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="16b89-120">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="16b89-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="16b89-121">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="16b89-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="16b89-122">Les formats de surface déterminent la façon dont les données pour chaque pixel de la mémoire de surface sont interprétées.</span><span class="sxs-lookup"><span data-stu-id="16b89-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="16b89-123">Direct3D utilise le membre [D3DFORMAT](d3dformat.md) de la structure [**D3DSURFACE \_ desc**](d3dsurface-desc.md) pour décrire le format de surface.</span><span class="sxs-lookup"><span data-stu-id="16b89-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="16b89-124">Vous pouvez récupérer le format d’une surface existante en appelant la méthode [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .</span><span class="sxs-lookup"><span data-stu-id="16b89-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="16b89-125">Une fois qu’une surface est créée, vous pouvez obtenir un pointeur vers celle-ci en appelant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="16b89-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="16b89-126">**GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="16b89-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="16b89-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="16b89-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="16b89-128">**GetDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="16b89-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="16b89-129">**GetFrontBufferData**</span><span class="sxs-lookup"><span data-stu-id="16b89-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="16b89-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="16b89-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="16b89-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="16b89-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="16b89-132">**GetSurfaceLevel**</span><span class="sxs-lookup"><span data-stu-id="16b89-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="16b89-133">L’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) vous permet d’accéder indirectement à la mémoire par le biais de la méthode [**UpdateSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="16b89-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="16b89-134">Cette méthode vous permet de copier une zone rectangulaire de pixels d’une interface **IDirect3DSurface9** vers une autre interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="16b89-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="16b89-135">L’interface surface possède également des méthodes pour accéder directement à la mémoire d’affichage.</span><span class="sxs-lookup"><span data-stu-id="16b89-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="16b89-136">Par exemple, vous pouvez utiliser la méthode [**LockRect**](/windows/desktop/api) pour verrouiller une zone rectangulaire de mémoire d’affichage.</span><span class="sxs-lookup"><span data-stu-id="16b89-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="16b89-137">Il est important d’appeler [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) une fois que vous avez fini d’utiliser la zone rectangulaire verrouillée sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="16b89-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="16b89-138">Rubriques supplémentaires sur la surface</span><span class="sxs-lookup"><span data-stu-id="16b89-138">Additional Surface Topics</span></span>

<span data-ttu-id="16b89-139">Apprenez-en davantage sur l’utilisation des surfaces avec l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="16b89-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="16b89-140">Formats de surface (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="16b89-141">Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="16b89-142">Largeur et inclinaison (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="16b89-143">Retournement des surfaces (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="16b89-144">Mise en mémoire tampon de basculement et de page (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="16b89-145">Copier dans des surfaces (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="16b89-146">Copie de surfaces (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="16b89-147">Accès direct à la mémoire de surface (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="16b89-148">Données de surface privée (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="16b89-149">Contrôles gamma (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="16b89-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="16b89-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16b89-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b89-151">Prise en main</span><span class="sxs-lookup"><span data-stu-id="16b89-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
