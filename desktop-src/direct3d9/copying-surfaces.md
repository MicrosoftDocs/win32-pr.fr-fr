---
description: Le terme blit est raccourci pour &\# 0034 ; transfert de blocs binaires, &\# 0034 ; il s’agit du processus de transfert des blocs de données d’un emplacement à un autre dans la mémoire.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copie de surfaces (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514542"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="ab7ac-103">Copie de surfaces (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ab7ac-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="ab7ac-104">Le terme blit est raccourci pour « transfert de blocs binaires », qui est le processus de transfert des blocs de données d’un emplacement à un autre dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="ab7ac-105">L’interface de pilote de périphérique (DDI) blitting continue à être utilisée dans Direct3D 9 comme mécanisme principal pour déplacer de grands rectangles de pixels en fonction de la trame, le mécanisme sous-jacent de la méthode de IDirect3DDevice9 de copie [**::P**](/windows/desktop/api) renouvelée.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ab7ac-106">Le transport de l’illustration dans l’opération blit est effectué par la méthode [**IDirect3DDevice9 :: UpdateTexture**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ab7ac-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ab7ac-107">L’illustration peut également être copiée dans Direct3D 9 à l’aide de la méthode [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , qui copie un sous-ensemble rectangulaire de pixels.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="ab7ac-108">Direct3D 9 fournit des fonctions D3DX qui vous permettent de charger des illustrations à partir de fichiers, d’appliquer une conversion des couleurs et de redimensionner des illustrations.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="ab7ac-109">Pour plus d’informations sur les fonctions disponibles [, consultez fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="ab7ac-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ab7ac-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab7ac-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab7ac-111">Surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="ab7ac-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="ab7ac-112">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="ab7ac-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="ab7ac-113">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="ab7ac-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
