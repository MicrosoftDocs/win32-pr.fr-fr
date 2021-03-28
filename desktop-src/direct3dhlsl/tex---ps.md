---
title: Tex-PS
description: Charge le registre de destination avec les données de couleur (RVBA) échantillonnées à partir d’une texture. La texture doit être liée à une étape de texture particulière (n) à l’aide de SetTexture. L’échantillonnage de texture est contrôlé par SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941146"
---
# <a name="tex---ps"></a><span data-ttu-id="5a47a-105">Tex-PS</span><span class="sxs-lookup"><span data-stu-id="5a47a-105">tex - ps</span></span>

<span data-ttu-id="5a47a-106">Charge le registre de destination avec les données de couleur (RVBA) échantillonnées à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="5a47a-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="5a47a-107">La texture doit être liée à une étape de texture particulière (n) à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="5a47a-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="5a47a-108">L’échantillonnage de texture est contrôlé par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="5a47a-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a47a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a47a-109">Syntax</span></span>



| <span data-ttu-id="5a47a-110">Tex DST</span><span class="sxs-lookup"><span data-stu-id="5a47a-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="5a47a-111">where</span><span class="sxs-lookup"><span data-stu-id="5a47a-111">where</span></span>

-   <span data-ttu-id="5a47a-112">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="5a47a-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a47a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5a47a-113">Remarks</span></span>



| <span data-ttu-id="5a47a-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a47a-114">Pixel shader versions</span></span> | <span data-ttu-id="5a47a-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5a47a-115">1\_1</span></span> | <span data-ttu-id="5a47a-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="5a47a-116">1\_2</span></span> | <span data-ttu-id="5a47a-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5a47a-117">1\_3</span></span> | <span data-ttu-id="5a47a-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="5a47a-118">1\_4</span></span> | <span data-ttu-id="5a47a-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a47a-119">2\_0</span></span> | <span data-ttu-id="5a47a-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a47a-120">2\_x</span></span> | <span data-ttu-id="5a47a-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5a47a-121">2\_sw</span></span> | <span data-ttu-id="5a47a-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a47a-122">3\_0</span></span> | <span data-ttu-id="5a47a-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5a47a-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5a47a-124">Tex</span><span class="sxs-lookup"><span data-stu-id="5a47a-124">tex</span></span>                   | <span data-ttu-id="5a47a-125">x</span><span class="sxs-lookup"><span data-stu-id="5a47a-125">x</span></span>    | <span data-ttu-id="5a47a-126">x</span><span class="sxs-lookup"><span data-stu-id="5a47a-126">x</span></span>    | <span data-ttu-id="5a47a-127">x</span><span class="sxs-lookup"><span data-stu-id="5a47a-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="5a47a-128">Le numéro de registre de destination spécifie le numéro de l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="5a47a-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="5a47a-129">L’échantillonnage de texture utilise des coordonnées de texture pour rechercher, ou échantillonner, une valeur de couleur aux coordonnées spécifiées (u, v, w, q) tout en tenant compte des attributs d’état de la phase de texture.</span><span class="sxs-lookup"><span data-stu-id="5a47a-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="5a47a-130">Les données de coordonnée de texture sont interpolées à partir des données de coordonnée de texture de vertex et sont associées à une étape de texture spécifique.</span><span class="sxs-lookup"><span data-stu-id="5a47a-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="5a47a-131">L’Association par défaut est un mappage un-à-un entre le numéro de l’étape de texture et l’ordre de déclaration des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="5a47a-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="5a47a-132">Cela signifie que le premier jeu de coordonnées de texture défini dans le format de vertex est associé par défaut à l’étape de texture 0.</span><span class="sxs-lookup"><span data-stu-id="5a47a-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="5a47a-133">Les coordonnées de texture peuvent être associées à n’importe quelle étape à l’aide de deux techniques.</span><span class="sxs-lookup"><span data-stu-id="5a47a-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="5a47a-134">Lors de l’utilisation d’un nuanceur de sommets de fonction fixe ou du pipeline de fonction fixe, l’indicateur d’état de l’étape de texture TSS \_ TEXCOORDINDEX peut être utilisé dans [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) pour associer des coordonnées à une étape.</span><span class="sxs-lookup"><span data-stu-id="5a47a-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="5a47a-135">Sinon, les coordonnées de texture sont générées par le nuanceur de sommets oTn s’inscrit lors de l’utilisation d’un nuanceur de sommet programmable.</span><span class="sxs-lookup"><span data-stu-id="5a47a-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a47a-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a47a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a47a-137">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a47a-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 