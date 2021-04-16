---
description: Direct3D utilise une forme de filtrage de texture linéaire appelée Filtrage bilinéaire.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtrage de texture linéaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521927"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="2b9a3-103">Filtrage de texture linéaire (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b9a3-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="2b9a3-104">Direct3D utilise une forme de filtrage de texture linéaire appelée Filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="2b9a3-105">À l’instar [de l’échantillonnage à point le plus proche (Direct3D 9)](nearest-point-sampling.md), le filtrage de texture bilinéaire calcule d’abord une adresse Texel, qui n’est généralement pas une adresse d’entier.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="2b9a3-106">Le filtrage bilinéaire recherche ensuite l’Texel dont l’adresse entière est la plus proche de l’adresse calculée.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="2b9a3-107">En outre, le module de rendu Direct3D calcule une moyenne pondérée des texels immédiatement au-dessus, en dessous, à gauche et à droite du point d’échantillonnage le plus proche.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="2b9a3-108">Sélectionnez le filtrage de texture bilinéaire en appelant la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="2b9a3-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="2b9a3-109">Définissez la valeur du premier paramètre sur le numéro d’index entier (0-7) de la texture pour laquelle vous sélectionnez une méthode de filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="2b9a3-110">Transmettez D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER pour le deuxième paramètre afin de définir le filtre d’agrandissement, de minimisation ou de mappage MIP.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="2b9a3-111">Transmettez D3DTEXF \_ Linear dans le troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b9a3-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b9a3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9a3-113">Filtrage de texture</span><span class="sxs-lookup"><span data-stu-id="2b9a3-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
