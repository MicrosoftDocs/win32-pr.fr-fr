---
title: texkill-PS
description: Annule le rendu du pixel actuel si l’un des trois premiers composants (UVW) des coordonnées de texture est inférieur à zéro.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313615"
---
# <a name="texkill---ps"></a><span data-ttu-id="934cc-103">texkill-PS</span><span class="sxs-lookup"><span data-stu-id="934cc-103">texkill - ps</span></span>

<span data-ttu-id="934cc-104">Annule le rendu du pixel actuel si l’un des trois premiers composants (UVW) des coordonnées de texture est inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="934cc-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="934cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="934cc-105">Syntax</span></span>



| <span data-ttu-id="934cc-106">texkill DST</span><span class="sxs-lookup"><span data-stu-id="934cc-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="934cc-107">where</span><span class="sxs-lookup"><span data-stu-id="934cc-107">where</span></span>

-   <span data-ttu-id="934cc-108">l’heure d’été est un registre de destination</span><span class="sxs-lookup"><span data-stu-id="934cc-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="934cc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="934cc-109">Remarks</span></span>



| <span data-ttu-id="934cc-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="934cc-110">Pixel shader versions</span></span> | <span data-ttu-id="934cc-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="934cc-111">1\_1</span></span> | <span data-ttu-id="934cc-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="934cc-112">1\_2</span></span> | <span data-ttu-id="934cc-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="934cc-113">1\_3</span></span> | <span data-ttu-id="934cc-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="934cc-114">1\_4</span></span> | <span data-ttu-id="934cc-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="934cc-115">2\_0</span></span> | <span data-ttu-id="934cc-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="934cc-116">2\_x</span></span> | <span data-ttu-id="934cc-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="934cc-117">2\_sw</span></span> | <span data-ttu-id="934cc-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="934cc-118">3\_0</span></span> | <span data-ttu-id="934cc-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="934cc-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="934cc-120">texkill</span><span class="sxs-lookup"><span data-stu-id="934cc-120">texkill</span></span>               | <span data-ttu-id="934cc-121">x</span><span class="sxs-lookup"><span data-stu-id="934cc-121">x</span></span>    | <span data-ttu-id="934cc-122">x</span><span class="sxs-lookup"><span data-stu-id="934cc-122">x</span></span>    | <span data-ttu-id="934cc-123">x</span><span class="sxs-lookup"><span data-stu-id="934cc-123">x</span></span>    | <span data-ttu-id="934cc-124">x</span><span class="sxs-lookup"><span data-stu-id="934cc-124">x</span></span>    | <span data-ttu-id="934cc-125">x</span><span class="sxs-lookup"><span data-stu-id="934cc-125">x</span></span>    | <span data-ttu-id="934cc-126">x</span><span class="sxs-lookup"><span data-stu-id="934cc-126">x</span></span>    | <span data-ttu-id="934cc-127">x</span><span class="sxs-lookup"><span data-stu-id="934cc-127">x</span></span>     | <span data-ttu-id="934cc-128">x</span><span class="sxs-lookup"><span data-stu-id="934cc-128">x</span></span>    | <span data-ttu-id="934cc-129">x</span><span class="sxs-lookup"><span data-stu-id="934cc-129">x</span></span>     |



 

<span data-ttu-id="934cc-130">Cette instruction correspond à la fonction de [**découpage**](dx-graphics-hlsl-clip.md) du langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="934cc-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="934cc-131">texkill n’échantillonne aucune texture.</span><span class="sxs-lookup"><span data-stu-id="934cc-131">texkill does not sample any texture.</span></span> <span data-ttu-id="934cc-132">Il opère sur les trois premiers composants des coordonnées de texture fournies par le numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="934cc-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="934cc-133">Pour PS \_ 1 \_ 4, texkill fonctionne sur les données dans les trois premiers composants du registre de destination.</span><span class="sxs-lookup"><span data-stu-id="934cc-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="934cc-134">Vous pouvez utiliser cette instruction pour implémenter des plans de clips arbitraires dans le rastériseur.</span><span class="sxs-lookup"><span data-stu-id="934cc-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="934cc-135">Lorsque vous utilisez des nuanceurs vertex, l’application est responsable de l’application de la transformation de perspective.</span><span class="sxs-lookup"><span data-stu-id="934cc-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="934cc-136">Cela peut entraîner des problèmes pour les plans de découpage arbitraires, car s’ils contiennent des facteurs d’échelle anisomorphic, les plans de clip doivent également être transformés.</span><span class="sxs-lookup"><span data-stu-id="934cc-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="934cc-137">Par conséquent, il est préférable de fournir une position de vertex non projetée à utiliser dans le Clipper arbitraire, qui est le jeu de coordonnées de texture identifié par l’opérateur texkill.</span><span class="sxs-lookup"><span data-stu-id="934cc-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="934cc-138">Cette instruction est utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="934cc-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="934cc-139">texkill TN</span><span class="sxs-lookup"><span data-stu-id="934cc-139">texkill tn</span></span>  
<span data-ttu-id="934cc-140">Le masquage des pixels s’effectue comme suit :</span><span class="sxs-lookup"><span data-stu-id="934cc-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="934cc-141">if (les composants x, y, z de TextureCoordinates (stage n)<sub>UVWQ</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="934cc-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="934cc-142">annuler le rendu de pixel</span><span class="sxs-lookup"><span data-stu-id="934cc-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="934cc-143">Pour le nuanceur de pixels 1 \_ 1, 1 \_ 2 et 1 \_ 3, texkill opère sur le jeu de coordonnées de texture donné par le numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="934cc-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="934cc-144">Dans la version 1 \_ 4, toutefois, texkill fonctionne sur les données contenues dans le [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) ou dans le registre temporaire (RN) qui a été spécifié comme destination.</span><span class="sxs-lookup"><span data-stu-id="934cc-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="934cc-145">Lorsque l’échantillonnage multiple est activé, tout effet d’anticrénelage atteint sur les arêtes de polygones en raison de l’échantillonnage multiple n’est pas effectué sur un bord qui a été généré par texkill.</span><span class="sxs-lookup"><span data-stu-id="934cc-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="934cc-146">Le nuanceur de pixels s’exécute une fois par pixel.</span><span class="sxs-lookup"><span data-stu-id="934cc-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="934cc-147">Cet exemple n'est donné qu'à titre indicatif.</span><span class="sxs-lookup"><span data-stu-id="934cc-147">This example is for illustration only.</span></span>

<span data-ttu-id="934cc-148">Cet exemple masque les pixels qui ont des coordonnées de texture négatives.</span><span class="sxs-lookup"><span data-stu-id="934cc-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="934cc-149">Les couleurs de pixel sont interpolées à partir des couleurs de vertex fournies dans les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="934cc-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="934cc-150">Les coordonnées de texture sont comprises entre-0,5 et 0,5 dans u, et 0,0 à 1,0 dans v.</span><span class="sxs-lookup"><span data-stu-id="934cc-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="934cc-151">Cette instruction entraîne le masquage des valeurs d’u négatives. La première illustration ci-dessous montre la couleur de vertex appliquée au Quad sans l’instruction texkill appliquée.</span><span class="sxs-lookup"><span data-stu-id="934cc-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="934cc-152">La deuxième illustration suivante montre le résultat de l’instruction texkill.</span><span class="sxs-lookup"><span data-stu-id="934cc-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="934cc-153">Les couleurs de pixel des coordonnées de texture inférieures à 0 (où x passe de-0,5 à 0,0) sont masquées. La couleur d’arrière-plan (blanc) est utilisée pour masquer la couleur de pixel.</span><span class="sxs-lookup"><span data-stu-id="934cc-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![illustration de la sortie avec la couleur de vertex appliquée au Quad sans l’instruction texkill](images/pstexkill-in.jpg)![illustration de la sortie avec l’instruction texkill appliquée](images/pstexkill-out.jpg)

<span data-ttu-id="934cc-156">Les données de coordonnée de texture sont déclarées dans la déclaration de données de vertex dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="934cc-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="934cc-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="934cc-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="934cc-158">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="934cc-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




