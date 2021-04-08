---
description: Le modèle Vertex Shader 3,0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de l’instruction texldl-vs texture Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Textures de vertex dans vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747157"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="bfb22-103">Textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfb22-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="bfb22-104">Le modèle Vertex Shader 3,0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de l’instruction [texldl-vs](../direct3dhlsl/texldl---vs.md) texture Load.</span><span class="sxs-lookup"><span data-stu-id="bfb22-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="bfb22-105">Le moteur vertex contient quatre étapes d’échantillonnage de texture, nommées [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 et D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="bfb22-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="bfb22-106">Celles-ci sont distinctes de l’échantillonneur de mappage et des échantillonneurs de texture dans le moteur de pixels.</span><span class="sxs-lookup"><span data-stu-id="bfb22-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="bfb22-107">Pour échantillonner les textures à ces quatre étapes, vous pouvez utiliser le moteur de vertex et programmer les étapes avec la méthode [**CheckDeviceFormat**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bfb22-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="bfb22-108">Définissez les textures à ces étapes à l’aide de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), avec l’index intermédiaire [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) jusqu’à D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="bfb22-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="bfb22-109">Un nouveau registre a été introduit dans le nuanceur de sommets, le registre de l’échantillonneur (comme dans PS \_ 2 \_ 0), qui représente l’échantillonneur de texture de vertex.</span><span class="sxs-lookup"><span data-stu-id="bfb22-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="bfb22-110">Ce registre doit être défini dans le nuanceur avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="bfb22-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="bfb22-111">Une application peut demander si un format est pris en charge en tant que texture de vertex en appelant [**CheckDeviceFormat**](/windows/desktop/api) avec [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md).</span><span class="sxs-lookup"><span data-stu-id="bfb22-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="bfb22-112">Il s’agit d’un indicateur de requête qui n’est pas accepté dans une fonction CreateXXX.</span><span class="sxs-lookup"><span data-stu-id="bfb22-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="bfb22-113">Une texture de vertex créée dans le pool par défaut peut être définie comme une texture de pixels et vice versa.</span><span class="sxs-lookup"><span data-stu-id="bfb22-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="bfb22-114">Toutefois, pour utiliser le traitement du vertex logiciel, la texture de vertex doit être créée dans le pool de Scratch (peu importe s’il s’agit d’un appareil en mode mixte ou d’un périphérique de traitement de vertex logiciel).</span><span class="sxs-lookup"><span data-stu-id="bfb22-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="bfb22-115">Les fonctionnalités sont identiques aux textures de pixels, à l’exception des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bfb22-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="bfb22-116">Le filtrage de texture anisotrope n’est pas pris en charge, c’est pourquoi D3DSAMP \_ MAXANISOTROPY est ignoré et D3DTEXF \_ anisotrope ne peut pas être défini pour la loupe, ou réduire pour ces étapes.</span><span class="sxs-lookup"><span data-stu-id="bfb22-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="bfb22-117">Le taux d’informations sur les modifications n’est pas disponible. par conséquent, l’application doit calculer le niveau de détail et fournir ces informations en tant que paramètre à [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bfb22-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="bfb22-118">Les restrictions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfb22-118">Restrictions include:</span></span>

-   <span data-ttu-id="bfb22-119">Comme dans les nuanceurs de pixels, si les textures multiéléments sont prises en charge, D3DSAMP \_ ELEMENTINDEX est utilisé pour déterminer l’élément à partir duquel échantillonner.</span><span class="sxs-lookup"><span data-stu-id="bfb22-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="bfb22-120">L’État D3DSAMP \_ DMAPOFFSET est ignoré pour ces étapes.</span><span class="sxs-lookup"><span data-stu-id="bfb22-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="bfb22-121">Utilisez [**CheckDeviceFormat**](/windows/desktop/api) avec [D3DUSAGE \_ query \_ VERTEXTEXTURE»](d3dusage-query.md) pour interroger une texture afin de déterminer si elle peut être utilisée comme texture de vertex.</span><span class="sxs-lookup"><span data-stu-id="bfb22-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="bfb22-122">VertexTextureFilterCaps indique le type de filtres qui sont autorisés au niveau des échantillonneurs de texture de vertex.</span><span class="sxs-lookup"><span data-stu-id="bfb22-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="bfb22-123">[D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) et D3DPTFILTERCAPS \_ MAGFANISOTROPIC ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="bfb22-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="bfb22-124">Registres des étapes d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="bfb22-124">Sampling Stage Registers</span></span>

<span data-ttu-id="bfb22-125">Un registre des étapes d’échantillonnage identifie une unité d’échantillonnage qui peut être utilisée dans les instructions de chargement de texture.</span><span class="sxs-lookup"><span data-stu-id="bfb22-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="bfb22-126">Une unité d’échantillonnage correspond à la phase d’échantillonnage de texture, en encapsulant l’état spécifique à l’échantillonnage fourni dans [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="bfb22-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="bfb22-127">Chaque échantillonneur identifie de façon unique une surface de texture unique qui est définie sur l’échantillonneur correspondant à l’aide de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="bfb22-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="bfb22-128">Toutefois, la même surface de texture peut être définie sur plusieurs échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="bfb22-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="bfb22-129">Au moment du tracé, une texture ne peut pas être définie simultanément comme une cible de rendu et une texture à une étape.</span><span class="sxs-lookup"><span data-stu-id="bfb22-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="bfb22-130">Étant donné que vs \_ 3 \_ 0 prend en charge quatre échantillonneurs, jusqu’à quatre surfaces de texture peuvent être lues à partir d’une seule passe de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bfb22-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="bfb22-131">Un registre d’échantillonnage peut apparaître uniquement comme argument dans l’instruction de chargement de texture : [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bfb22-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="bfb22-132">Dans vs \_ 3 \_ 0, si vous utilisez un échantillonneur, il doit être déclaré au début du programme Shader, à l’aide de la [DCL \_ samplerType (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (comme dans PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="bfb22-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="bfb22-133">Traitement logiciel</span><span class="sxs-lookup"><span data-stu-id="bfb22-133">Software Processing</span></span>

<span data-ttu-id="bfb22-134">Ce composant sera pris en charge dans le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="bfb22-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="bfb22-135">Les types de filtres spécifiques pris en charge peuvent être vérifiés en appelant [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) et en vérifiant VertexTextureFilterCaps.</span><span class="sxs-lookup"><span data-stu-id="bfb22-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="bfb22-136">Tous les formats de texture publiés seront pris en charge en tant que textures vertex dans le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="bfb22-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="bfb22-137">Les applications peuvent vérifier si un format de texture particulier est pris en charge dans le mode de traitement du vertex logiciel en appelant [**CheckDeviceFormat**](/windows/desktop/api) et en fournissant (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) comme utilisation.</span><span class="sxs-lookup"><span data-stu-id="bfb22-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="bfb22-138">Tous les formats sont pris en charge pour le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="bfb22-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="bfb22-139">Le pool de travail est requis pour le traitement des vertex logiciels.</span><span class="sxs-lookup"><span data-stu-id="bfb22-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="bfb22-140">Modifications de l’API</span><span class="sxs-lookup"><span data-stu-id="bfb22-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="bfb22-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bfb22-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfb22-142">Pipeline de vertex</span><span class="sxs-lookup"><span data-stu-id="bfb22-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
