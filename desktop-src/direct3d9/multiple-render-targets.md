---
description: Plusieurs cibles de rendu (MRT) se réfèrent à la possibilité d’effectuer un rendu sur plusieurs surfaces (consultez IDirect3D9Surface) avec un seul appel de dessin.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Plusieurs cibles de rendu (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482048"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="eacca-103">Plusieurs cibles de rendu (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="eacca-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="eacca-104">Plusieurs cibles de rendu (MRT) se réfèrent à la possibilité d’effectuer un rendu sur plusieurs surfaces (consultez [**IDirect3D9Surface**](/windows/desktop/api)) avec un seul appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="eacca-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="eacca-105">Ces surfaces peuvent être créées indépendamment les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="eacca-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="eacca-106">Les cibles de rendu peuvent être définies à l’aide de [**IDirect3DDevice9 :: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span><span class="sxs-lookup"><span data-stu-id="eacca-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="eacca-107">Plusieurs cibles de rendu présentent les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="eacca-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="eacca-108">Toutes les surfaces cibles de rendu utilisées ensemble doivent avoir la même profondeur de bits, mais elles peuvent être de différents formats, sauf si la limite D3DPMISCCAPS \_ MRTINDEPENDENTBITDEPTHS est définie.</span><span class="sxs-lookup"><span data-stu-id="eacca-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="eacca-109">Toutes les surfaces d’une cible de rendu multiple doivent avoir la même largeur et la même hauteur.</span><span class="sxs-lookup"><span data-stu-id="eacca-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="eacca-110">Certaines implémentations ne peuvent pas effectuer d’opérations de nuanceur de zéros sur plusieurs cibles de rendu, notamment : aucune trame, aucun test alpha, aucune transparence, aucune fusion ni masquage, à l’exception du test z-test et du stencil.</span><span class="sxs-lookup"><span data-stu-id="eacca-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="eacca-111">Les appareils qui prennent en charge les opérations de nuanceur après le pixel définissent le bit Cap sur D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.</span><span class="sxs-lookup"><span data-stu-id="eacca-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="eacca-112">Lorsque l' \_ embout D3DPMISCCAPS MRTPOSTPIXELSHADERBLENDING est défini, vous devez d’abord consulter le [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec la \_ requête \_ d’utilisation POSTPIXELSHADER le \_ résultat de fusion pour le format de surface spécifique.</span><span class="sxs-lookup"><span data-stu-id="eacca-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="eacca-113">Si la valeur est false, aucune opération de fusion de nuanceur de pixel postérieure n’est disponible pour ce format de surface spécifique.</span><span class="sxs-lookup"><span data-stu-id="eacca-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="eacca-114">Si la valeur est true, l’appareil est censé appliquer le même État à toutes les cibles de rendu simultanées comme suit :</span><span class="sxs-lookup"><span data-stu-id="eacca-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="eacca-115">Alpha Blend : la valeur de couleur dans oCi est mélangée avec la cible de rendu énième.</span><span class="sxs-lookup"><span data-stu-id="eacca-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="eacca-116">Test alpha : la comparaison aura lieu avec oC0.</span><span class="sxs-lookup"><span data-stu-id="eacca-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="eacca-117">Si la comparaison échoue, le test de pixel s’arrête pour toutes les cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="eacca-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="eacca-118">Brouillard : la cible de rendu 0 va s’afficher.</span><span class="sxs-lookup"><span data-stu-id="eacca-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="eacca-119">Les autres cibles de rendu ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="eacca-119">Other render targets are undefined.</span></span> <span data-ttu-id="eacca-120">Les implémentations peuvent choisir de les survoiler toutes en utilisant le même État.</span><span class="sxs-lookup"><span data-stu-id="eacca-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="eacca-121">Tramage : non défini.</span><span class="sxs-lookup"><span data-stu-id="eacca-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="eacca-122">Aucun anticrénelage n’est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="eacca-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="eacca-123">Certaines implémentations n’appliquent pas le masque d’écriture de sortie (D3DRS \_ COLORWRITEENABLE).</span><span class="sxs-lookup"><span data-stu-id="eacca-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="eacca-124">Ceux qui peuvent avoir des masques d’écriture de couleur indépendants.</span><span class="sxs-lookup"><span data-stu-id="eacca-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="eacca-125">Cela est exprimé à l’aide d’un nouveau bit de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eacca-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="eacca-126">Le nombre de masques d’écriture de couleur indépendants disponibles sera égal au nombre maximal d’éléments que l’appareil est en capacité de prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="eacca-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="eacca-127">Nouvelles extrémités matérielles :</span><span class="sxs-lookup"><span data-stu-id="eacca-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="eacca-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eacca-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eacca-129">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="eacca-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
