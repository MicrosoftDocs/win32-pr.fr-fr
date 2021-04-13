---
description: L’interface ID3DXTextureGutterHelper est utilisée pour créer et gérer des zones de marge dans une texture. Les régions de reliure séparent les textures et permettent l’interpolation bilinéaire afin d’éviter le rendu des artefacts aux limites de la texture.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interface ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323222"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="8e2ea-104">Interface ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="8e2ea-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="8e2ea-105">L’interface ID3DXTextureGutterHelper est utilisée pour créer et gérer des zones de marge dans une texture.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="8e2ea-106">Les régions de reliure séparent les textures et permettent l’interpolation bilinéaire afin d’éviter le rendu des artefacts aux limites de la texture.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="8e2ea-107">Le... les méthodes fournissent l’accès aux structures de données utilisées par l’application... leurs.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="8e2ea-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8e2ea-108">Members</span></span>

<span data-ttu-id="8e2ea-109">L’interface **ID3DXTextureGutterHelper** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8e2ea-110">**ID3DXTextureGutterHelper** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e2ea-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="8e2ea-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e2ea-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8e2ea-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e2ea-112">Methods</span></span>

<span data-ttu-id="8e2ea-113">L’interface **ID3DXTextureGutterHelper** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="8e2ea-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="8e2ea-114">Method</span></span>                                                                   | <span data-ttu-id="8e2ea-115">Description</span><span class="sxs-lookup"><span data-stu-id="8e2ea-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e2ea-116">**ApplyGuttersFloat**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="8e2ea-117">Applique des reliures à une mémoire tampon de texture FLOTTante.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="8e2ea-118">**ApplyGuttersPRT**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="8e2ea-119">Applique des gouttières à un objet de mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="8e2ea-120">**ApplyGuttersTex**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="8e2ea-121">Applique des gouttières à un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="8e2ea-122">**GetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="8e2ea-123">Récupère les coordonnées Barycentric texels.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="8e2ea-124">**GetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="8e2ea-125">Récupère l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="8e2ea-126">**GetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="8e2ea-127">Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="8e2ea-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="8e2ea-129">Récupère la hauteur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="8e2ea-130">**GetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="8e2ea-131">Récupère les coordonnées de texture (u, v) de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="8e2ea-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="8e2ea-133">Récupère la largeur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="8e2ea-134">**ResampleTex**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="8e2ea-135">Rééchantillonne une texture dans le paramétrage de ce gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="8e2ea-136">**SetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="8e2ea-137">Définit les coordonnées Barycentric texels.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="8e2ea-138">**SetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="8e2ea-139">Définit l’index du type de maillage auquel appartient chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="8e2ea-140">**SetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="8e2ea-141">Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="8e2ea-142">**SetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="8e2ea-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="8e2ea-143">Définit les coordonnées de texture (u, v) de chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="8e2ea-144">Notes</span><span class="sxs-lookup"><span data-stu-id="8e2ea-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8e2ea-145">Lorsqu’elle est utilisée avec le luminance de transfert précalculé (PRT), cette interface requiert un paramétrage unique du modèle.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="8e2ea-146">Chaque Texel doit correspondre à un point unique sur la surface du modèle et vice versa.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="8e2ea-147">Si le modèle comprend plusieurs textures, celles-ci doivent être fractionnées en éléments distincts qui contiennent chacun un objet d’assistance de gouttière par texture.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="8e2ea-148">Cette interface peut être utilisée pour générer un mappage dans l’espace de texture dans lequel chaque Texel est dans l’une des quatre classes.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="8e2ea-149">Texel (classe)</span><span class="sxs-lookup"><span data-stu-id="8e2ea-149">Texel Class</span></span> | <span data-ttu-id="8e2ea-150">Emplacement de Texel</span><span class="sxs-lookup"><span data-stu-id="8e2ea-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2ea-151">0</span><span class="sxs-lookup"><span data-stu-id="8e2ea-151">0</span></span>           | <span data-ttu-id="8e2ea-152">Point non valide ; Texel ne sera pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8e2ea-153">1</span><span class="sxs-lookup"><span data-stu-id="8e2ea-153">1</span></span>           | <span data-ttu-id="8e2ea-154">Triangle intérieur.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8e2ea-155">2</span><span class="sxs-lookup"><span data-stu-id="8e2ea-155">2</span></span>           | <span data-ttu-id="8e2ea-156">Marge intérieure.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8e2ea-157">4</span><span class="sxs-lookup"><span data-stu-id="8e2ea-157">4</span></span>           | <span data-ttu-id="8e2ea-158">Marge intérieure ; Texel sera évalué comme un exemple complet dans les méthodes [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper :: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper :: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="8e2ea-159">Pour les classes 1 et 2, un Texel est stocké avec la face à laquelle il appartient, ainsi que les coordonnées Barycentric des deux premiers sommets de ce visage.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="8e2ea-160">Les sommets de la reliure sont affectés au bord le plus proche dans l’espace de texture.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="8e2ea-161">Il n’existe pas de classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="8e2ea-161">There is no texel class 3.</span></span>

<span data-ttu-id="8e2ea-162">L’interface **ID3DXTextureGutterHelper** est obtenue en appelant la fonction [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="8e2ea-163">Le type LPD3DXTEXTUREGUTTERHELPER est défini comme un pointeur vers l’interface **ID3DXTextureGutterHelper** .</span><span class="sxs-lookup"><span data-stu-id="8e2ea-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="8e2ea-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e2ea-164">Requirements</span></span>



| <span data-ttu-id="8e2ea-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e2ea-165">Requirement</span></span> | <span data-ttu-id="8e2ea-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e2ea-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2ea-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e2ea-167">Header</span></span><br/>  | <dl> <span data-ttu-id="8e2ea-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e2ea-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8e2ea-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e2ea-169">Library</span></span><br/> | <dl> <span data-ttu-id="8e2ea-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e2ea-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e2ea-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e2ea-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e2ea-172">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8e2ea-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
