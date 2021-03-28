---
title: texcoord-PS
description: Interprète les données de coordonnée de texture (UVW1) en tant que données de couleur (RVBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728060"
---
# <a name="texcoord---ps"></a><span data-ttu-id="7d4ab-103">texcoord-PS</span><span class="sxs-lookup"><span data-stu-id="7d4ab-103">texcoord - ps</span></span>

<span data-ttu-id="7d4ab-104">Interprète les données de coordonnée de texture (UVW1) en tant que données de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d4ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d4ab-105">Syntax</span></span>



| <span data-ttu-id="7d4ab-106">texcoord DST</span><span class="sxs-lookup"><span data-stu-id="7d4ab-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="7d4ab-107">where</span><span class="sxs-lookup"><span data-stu-id="7d4ab-107">where</span></span>

-   <span data-ttu-id="7d4ab-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d4ab-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7d4ab-109">Remarks</span></span>



| <span data-ttu-id="7d4ab-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7d4ab-110">Pixel shader versions</span></span> | <span data-ttu-id="7d4ab-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="7d4ab-111">1\_1</span></span> | <span data-ttu-id="7d4ab-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="7d4ab-112">1\_2</span></span> | <span data-ttu-id="7d4ab-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7d4ab-113">1\_3</span></span> | <span data-ttu-id="7d4ab-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="7d4ab-114">1\_4</span></span> | <span data-ttu-id="7d4ab-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d4ab-115">2\_0</span></span> | <span data-ttu-id="7d4ab-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d4ab-116">2\_x</span></span> | <span data-ttu-id="7d4ab-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="7d4ab-117">2\_sw</span></span> | <span data-ttu-id="7d4ab-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d4ab-118">3\_0</span></span> | <span data-ttu-id="7d4ab-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="7d4ab-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7d4ab-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="7d4ab-120">texcoord</span></span>              | <span data-ttu-id="7d4ab-121">x</span><span class="sxs-lookup"><span data-stu-id="7d4ab-121">x</span></span>    | <span data-ttu-id="7d4ab-122">x</span><span class="sxs-lookup"><span data-stu-id="7d4ab-122">x</span></span>    | <span data-ttu-id="7d4ab-123">x</span><span class="sxs-lookup"><span data-stu-id="7d4ab-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7d4ab-124">Cette instruction interprète le jeu de coordonnées de texture (UVW1) correspondant au numéro de registre de destination en tant que données de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="7d4ab-125">Si le jeu de coordonnées de texture contient moins de trois composants, les composants manquants ont la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="7d4ab-126">Le quatrième composant est toujours défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="7d4ab-127">Toutes les valeurs sont ancrées entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="7d4ab-128">L’avantage de texcoord est qu’il fournit un moyen de passer des données de vertex interpolées à haute précision directement dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="7d4ab-129">Toutefois, lorsque les données sont écrites dans le registre de destination, une certaine précision est perdue, en fonction du nombre de bits utilisés par le matériel pour les registres.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="7d4ab-130">Aucune texture n’est échantillonnée par cette instruction.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="7d4ab-131">Seules les coordonnées de texture définies pour cette étape de texture sont pertinentes.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="7d4ab-132">Toutes les données de texture (telles que la position, la normale et la direction de la source de lumière) peuvent être mappées par un nuanceur de sommets à une coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="7d4ab-133">Pour ce faire, associez une texture à un registre de texture à l’aide de [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) et spécifiez comment l’échantillonnage de texture est effectué à l’aide de [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="7d4ab-134">Si le pipeline de fonction fixe est utilisé, veillez à fournir l' \_ indicateur TSS TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="7d4ab-135">Cette instruction est utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d4ab-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="7d4ab-136">Un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contient quatre valeurs de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="7d4ab-137">Les données peuvent également être considérées comme des données vectorielles (XYZW).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="7d4ab-138">texcoord récupère trois de ces valeurs (XYZ) à partir du jeu de coordonnées de texture x et le quatrième composant (w) a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="7d4ab-139">L’adresse de texture est copiée à partir du jeu de coordonnées de texture n.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="7d4ab-140">Le résultat est bloqué entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="7d4ab-141">Cet exemple n'est donné qu'à titre indicatif.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-141">This example is for illustration only.</span></span> <span data-ttu-id="7d4ab-142">Le code C qui accompagne le nuanceur n’a pas été optimisé pour les performances.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="7d4ab-143">Voici un exemple de nuanceur utilisant texcoord.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="7d4ab-144">La sortie rendue par le nuanceur de pixels est présentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="7d4ab-145">Les valeurs de coordonnée (u, v, w, 1) sont mappées aux canaux (RVB).</span><span class="sxs-lookup"><span data-stu-id="7d4ab-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="7d4ab-146">Le canal alpha est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="7d4ab-147">Aux angles de l’illustration, la coordonnée (0, 0, 0, 1) est interprétée comme noir ; (1, 0, 0, 1) est rouge ; (0, 1, 0, 1) est vert ; et (1, 1, 0, 1) contient le vert et le rouge, ce qui produit le jaune.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![illustration de la sortie rendue de l’exemple de nuanceur de pixels](images/pstexcoord.jpg)

<span data-ttu-id="7d4ab-149">Du code supplémentaire est nécessaire pour utiliser ce nuanceur et un exemple de scénario est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7d4ab-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="7d4ab-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d4ab-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d4ab-151">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7d4ab-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 