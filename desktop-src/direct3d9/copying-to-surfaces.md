---
description: 'Quand vous utilisez IDirect3DDevice9 :: UpdateSurface, transmettez un rectangle sur la surface source, ou utilisez la valeur NULL pour spécifier la surface entière.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copier dans des surfaces (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483840"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="cadb2-103">Copier dans des surfaces (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cadb2-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="cadb2-104">Quand vous utilisez [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), transmettez un rectangle sur la surface source, ou utilisez la **valeur null** pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="cadb2-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="cadb2-105">Vous pouvez également passer un point sur la surface de destination vers laquelle la position supérieure gauche du rectangle sur l’image source est copiée.</span><span class="sxs-lookup"><span data-stu-id="cadb2-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="cadb2-106">Cette méthode ne prend pas en charge le découpage.</span><span class="sxs-lookup"><span data-stu-id="cadb2-106">This method does not support clipping.</span></span> <span data-ttu-id="cadb2-107">L’opération échouera à moins que le rectangle source et le rectangle de destination correspondant soient entièrement contenus dans les surfaces source et de destination, respectivement.</span><span class="sxs-lookup"><span data-stu-id="cadb2-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="cadb2-108">Cette méthode ne prend pas en charge la fusion alpha, les clés de couleur ou la conversion de format.</span><span class="sxs-lookup"><span data-stu-id="cadb2-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="cadb2-109">Notez que les surfaces source et de destination doivent être distinctes.</span><span class="sxs-lookup"><span data-stu-id="cadb2-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="cadb2-110">Pour d’autres restrictions lors de l’utilisation de UpdateSurface, consultez [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="cadb2-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="cadb2-111">Les méthodes suivantes sont également disponibles en C++/C pour copier des images sur une surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cadb2-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="cadb2-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="cadb2-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="cadb2-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="cadb2-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="cadb2-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="cadb2-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="cadb2-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="cadb2-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="cadb2-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="cadb2-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="cadb2-117">**IDirect3DDevice9::UpdateSurface**</span><span class="sxs-lookup"><span data-stu-id="cadb2-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="cadb2-118">Exemple UpdateSurface</span><span class="sxs-lookup"><span data-stu-id="cadb2-118">UpdateSurface Example</span></span>

<span data-ttu-id="cadb2-119">L’exemple suivant copie deux rectangles de la surface source vers une surface de destination.</span><span class="sxs-lookup"><span data-stu-id="cadb2-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="cadb2-120">Le premier rectangle est copié de (0, 0, 50, 50) sur la surface source vers le même emplacement sur la surface de destination, et le deuxième rectangle est copié de (50, 50, 100, 100) sur la surface source vers (150, 150, 200, 200) sur la surface de destination.</span><span class="sxs-lookup"><span data-stu-id="cadb2-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="cadb2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cadb2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cadb2-122">Surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="cadb2-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="cadb2-123">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="cadb2-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
