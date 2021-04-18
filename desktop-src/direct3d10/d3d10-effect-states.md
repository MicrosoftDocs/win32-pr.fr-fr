---
description: Les États d’effet sont des paires nom-valeur sous la forme d’une expression.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Groupes d’états d’effet (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321673"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="a93cd-103">Groupes d’états d’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a93cd-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="a93cd-104">Les États d’effet sont des paires nom-valeur sous la forme d’une expression.</span><span class="sxs-lookup"><span data-stu-id="a93cd-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="a93cd-105">État de fusion</span><span class="sxs-lookup"><span data-stu-id="a93cd-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="a93cd-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="a93cd-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="a93cd-107">Membres de [ **D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="a93cd-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="a93cd-108">État de la profondeur et du stencil</span><span class="sxs-lookup"><span data-stu-id="a93cd-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="a93cd-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="a93cd-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="a93cd-110">Membres de la [ **\_ Description du \_ stencil \_ de profondeur D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="a93cd-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="a93cd-111">FRONTFACESTENCILFAIL \* \*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="a93cd-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="a93cd-112">Membre de [ **D3D10 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="a93cd-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="a93cd-113">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="a93cd-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="a93cd-114">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="a93cd-114">FILLMODE</span></span> | [<span data-ttu-id="a93cd-115">**\_Mode de remplissage D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="a93cd-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="a93cd-116">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="a93cd-116">CULLMODE</span></span> | [<span data-ttu-id="a93cd-117">**\_Mode d’élimination D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="a93cd-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="a93cd-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a93cd-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="a93cd-119">Membres de [ **D3D10 \_ rastériseur \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="a93cd-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="a93cd-120">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="a93cd-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="a93cd-121">**Filter**,  **adAddressW**, **AddressV**,, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="a93cd-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="a93cd-122">Membres de l' [ **\_ échantillonneur D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="a93cd-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="a93cd-123">Pour obtenir des exemples, consultez [type d’échantillonneur (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="a93cd-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="a93cd-124">État de l’objet d’effet</span><span class="sxs-lookup"><span data-stu-id="a93cd-124">Effect object state</span></span>

| <span data-ttu-id="a93cd-125">Cet objet Effect</span><span class="sxs-lookup"><span data-stu-id="a93cd-125">This effect object</span></span> | <span data-ttu-id="a93cd-126">Correspond à</span><span class="sxs-lookup"><span data-stu-id="a93cd-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="a93cd-127">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="a93cd-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="a93cd-128">Objet d’état de l' [État du rastériseur](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="a93cd-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="a93cd-129">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="a93cd-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="a93cd-130">Objet d’état de [profondeur et](#depth-and-stencil-state) d’état de gabarit.</span><span class="sxs-lookup"><span data-stu-id="a93cd-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="a93cd-131">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="a93cd-131">BLENDSTATE</span></span> | <span data-ttu-id="a93cd-132">Objet d’état de l' [État de fusion](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="a93cd-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="a93cd-133">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="a93cd-133">VERTEXSHADER</span></span> | <span data-ttu-id="a93cd-134">Objet de nuanceur de sommets compilé.</span><span class="sxs-lookup"><span data-stu-id="a93cd-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="a93cd-135">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="a93cd-135">PIXELSHADER</span></span> | <span data-ttu-id="a93cd-136">Objet de nuanceur de pixels compilé.</span><span class="sxs-lookup"><span data-stu-id="a93cd-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="a93cd-137">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="a93cd-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="a93cd-138">Objet de nuanceur Geometry compilé.</span><span class="sxs-lookup"><span data-stu-id="a93cd-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="a93cd-139">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="a93cd-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="a93cd-140">Membres de [**D3D10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="a93cd-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="a93cd-141">Définition et utilisation d’objets d’État</span><span class="sxs-lookup"><span data-stu-id="a93cd-141">Defining and using state objects</span></span>

<span data-ttu-id="a93cd-142">Les objets d’État sont déclarés dans des fichiers FX au format suivant.</span><span class="sxs-lookup"><span data-stu-id="a93cd-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="a93cd-143">*StateObjectType* est l’un des États indiqués ci-dessus, et *MemberName* est le nom d’un membre qui aura une valeur non définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a93cd-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="a93cd-144">Par exemple, pour configurer un objet d’état de fusion avec AlphaToCoverageEnable et BlendEnable \[ 0 ayant \] la valeur **false**, le code suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a93cd-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="a93cd-145">L’objet d’État est appliqué à une technique Pass à l’aide de l’une des fonctions SetStateGroup décrites dans syntaxe de la [technique Effect (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a93cd-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="a93cd-146">Par exemple, pour appliquer l’objet BlendState décrit ci-dessus, vous devez utiliser le code suivant.</span><span class="sxs-lookup"><span data-stu-id="a93cd-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="a93cd-147">Pour obtenir un didacticiel décrivant l’utilisation des États, consultez Gestion de l' [État](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="a93cd-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a93cd-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a93cd-148">Related topics</span></span>

* [<span data-ttu-id="a93cd-149">Syntaxe de la technique Effect</span><span class="sxs-lookup"><span data-stu-id="a93cd-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="a93cd-150">Format d’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a93cd-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
