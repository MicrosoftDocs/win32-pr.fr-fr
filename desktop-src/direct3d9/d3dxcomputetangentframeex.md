---
description: Effectue des calculs de trame tangente sur une maille. Les vecteurs tangente, Binormal et éventuellement normaux sont générés. Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: D3DXComputeTangentFrameEx, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545269"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="cea2c-105">D3DXComputeTangentFrameEx fonction)</span><span class="sxs-lookup"><span data-stu-id="cea2c-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="cea2c-106">Effectue des calculs de trame tangente sur une maille.</span><span class="sxs-lookup"><span data-stu-id="cea2c-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="cea2c-107">Les vecteurs tangente, Binormal et éventuellement normaux sont générés.</span><span class="sxs-lookup"><span data-stu-id="cea2c-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="cea2c-108">Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex.</span><span class="sxs-lookup"><span data-stu-id="cea2c-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea2c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cea2c-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="cea2c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cea2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea2c-111">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-112">Type : **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cea2c-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cea2c-113">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cea2c-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-114">*dwTextureInSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-116">Spécifie la sémantique d’entrée de la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="cea2c-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="cea2c-117">Si D3DX \_ default, la fonction suppose qu’il n’y a pas de coordonnées de texture, et la fonction échoue à moins que le calcul de vecteur normal soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="cea2c-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-118">*dwTextureInIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-119">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-120">Si un maillage a plusieurs coordonnées de texture, spécifie la coordonnée de texture à utiliser pour les calculs de frame de tangente.</span><span class="sxs-lookup"><span data-stu-id="cea2c-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="cea2c-121">Si la valeur est zéro, le maillage n’a qu’une seule coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="cea2c-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-122">*dwUPartialOutSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-124">Spécifie la sémantique de sortie pour le type, généralement D3DDECLUSAGE \_ tangente, qui décrit où la coordonnée partielle par rapport à la coordonnée de la texture U sera stockée.</span><span class="sxs-lookup"><span data-stu-id="cea2c-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="cea2c-125">Si \_ la valeur par défaut est D3DX, cette dérivée partielle n’est pas stockée.</span><span class="sxs-lookup"><span data-stu-id="cea2c-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-126">*dwUPartialOutIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-128">Spécifie l’index sémantique auquel stocker le dérivée partiel par rapport à la coordonnée de texture U.</span><span class="sxs-lookup"><span data-stu-id="cea2c-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-129">*dwVPartialOutSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-131">Spécifie le type [**D3DDECLUSAGE**](./d3ddeclusage.md) , généralement D3DDECLUSAGE \_ binormal, qui décrit l’emplacement de stockage de la partie dérivée partielle par rapport à la coordonnée de texture V.</span><span class="sxs-lookup"><span data-stu-id="cea2c-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="cea2c-132">Si \_ la valeur par défaut est D3DX, cette dérivée partielle n’est pas stockée.</span><span class="sxs-lookup"><span data-stu-id="cea2c-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-133">*dwVPartialOutIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-135">Spécifie l’index sémantique au niveau duquel stocker la dérivée partielle par rapport à la coordonnée de texture V.</span><span class="sxs-lookup"><span data-stu-id="cea2c-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-136">*dwNormalOutSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-137">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-138">Spécifie la sémantique normale de sortie, généralement D3DDECLUSAGE \_ normal, qui décrit où le vecteur normal à chaque vertex sera stocké.</span><span class="sxs-lookup"><span data-stu-id="cea2c-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="cea2c-139">Si \_ la valeur par défaut est D3DX, ce vecteur normal n’est pas stocké.</span><span class="sxs-lookup"><span data-stu-id="cea2c-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-140">*dwNormalOutIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-141">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-142">Spécifie l’index sémantique à partir duquel stocker le vecteur normal à chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="cea2c-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-143">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-144">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-145">Combinaison d’un ou de plusieurs indicateurs [**D3DXTANGENT**](./d3dxtangent.md) qui spécifient des options de calcul de frame tangent.</span><span class="sxs-lookup"><span data-stu-id="cea2c-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="cea2c-146">Si la **valeur est null**, les options suivantes sont spécifiées :</span><span class="sxs-lookup"><span data-stu-id="cea2c-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="cea2c-147">Description</span><span class="sxs-lookup"><span data-stu-id="cea2c-147">Description</span></span>                                                                                              | <span data-ttu-id="cea2c-148">[**D3DXTANGENT**](./d3dxtangent.md) Valeur de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="cea2c-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cea2c-149">Pondérez la longueur du vecteur normal par l’angle, en radians, sous-tendus par les deux bords quittant le sommet.</span><span class="sxs-lookup"><span data-stu-id="cea2c-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="cea2c-150">& ! (D3DXTANGENT \_ POIDS \_ par \_ zone \| D3DXTANGENT \_ poids \_ égal)</span><span class="sxs-lookup"><span data-stu-id="cea2c-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="cea2c-151">Calculez les coordonnées Cartésienles orthogonales à partir des coordonnées de texture (u, v).</span><span class="sxs-lookup"><span data-stu-id="cea2c-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="cea2c-152">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cea2c-152">See Remarks.</span></span>                   | <span data-ttu-id="cea2c-153">& ! (D3DXTANGENT \_ ORTHOGONALiser \_ à partir de \_ U \| D3DXTANGENT \_ orthogonale \_ à partir de \_ V)</span><span class="sxs-lookup"><span data-stu-id="cea2c-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="cea2c-154">Les textures ne sont pas encapsulées dans les directions u ou v</span><span class="sxs-lookup"><span data-stu-id="cea2c-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="cea2c-155">& ! (D3DXTANGENT \_ ENVELOPPE \_ UV)</span><span class="sxs-lookup"><span data-stu-id="cea2c-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="cea2c-156">Les dérivés partiels en ce qui concerne les coordonnées de texture sont normalisés.</span><span class="sxs-lookup"><span data-stu-id="cea2c-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="cea2c-157">& ! (D3DXTANGENT \_ ne pas \_ normaliser les \_ partiels)</span><span class="sxs-lookup"><span data-stu-id="cea2c-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="cea2c-158">Les vertex sont triés dans le sens inverse des aiguilles d’une passe autour de chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="cea2c-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="cea2c-159">& ! (D3DXTANGENT \_ PV de vent \_ )</span><span class="sxs-lookup"><span data-stu-id="cea2c-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="cea2c-160">Utilisez des vecteurs normaux par vertex déjà présents dans le maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cea2c-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="cea2c-161">& ! (D3DXTANGENT \_ CALCULER les \_ normales)</span><span class="sxs-lookup"><span data-stu-id="cea2c-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="cea2c-162">Si \_ la génération \_ de D3DXTANGENT sur \_ place n’est pas définie, le maillage d’entrée est cloné.</span><span class="sxs-lookup"><span data-stu-id="cea2c-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="cea2c-163">La maille d’origine doit donc disposer d’un espace suffisant pour stocker le vecteur normal calculé et les données dérivées partielles.</span><span class="sxs-lookup"><span data-stu-id="cea2c-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-164">*pdwAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-165">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea2c-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cea2c-166">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="cea2c-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="cea2c-167">Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="cea2c-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-168">*fPartialEdgeThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-169">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-170">Spécifie le cosinus maximal de l’angle à partir duquel deux dérivés partiels sont considérés comme incompatibles entre eux.</span><span class="sxs-lookup"><span data-stu-id="cea2c-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="cea2c-171">Si le produit scalaire de la direction des deux dérivés partiels dans les triangles contigus est inférieur ou égal à ce seuil, les vertex partagés entre ces triangles seront fractionnés.</span><span class="sxs-lookup"><span data-stu-id="cea2c-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-172">*fSingularPointThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-173">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-174">Spécifie l’amplitude maximale d’une dérivée partielle à laquelle un vertex sera considéré comme singulier.</span><span class="sxs-lookup"><span data-stu-id="cea2c-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="cea2c-175">Comme plusieurs triangles sont des incidents sur un point qui ont des images tangentes proches, mais qui s’annulent complètement l’un de l’autre (par exemple, en haut d’une sphère), la grandeur de la dérivée partielle diminue.</span><span class="sxs-lookup"><span data-stu-id="cea2c-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="cea2c-176">Si la magnitude est inférieure ou égale à ce seuil, le vertex est fractionné pour chaque triangle qui le contient.</span><span class="sxs-lookup"><span data-stu-id="cea2c-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-177">*fNormalEdgeThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-178">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-179">Semblable à fPartialEdgeThreshold, spécifie le cosinus maximal de l’angle entre deux normales qui est un seuil au-delà duquel les vertex partagés entre triangles seront fractionnés.</span><span class="sxs-lookup"><span data-stu-id="cea2c-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="cea2c-180">Si le produit scalaire des deux normales est inférieur au seuil, les vertex partagés sont fractionnés, formant ainsi un bord fixe entre les triangles voisins.</span><span class="sxs-lookup"><span data-stu-id="cea2c-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="cea2c-181">Si le produit scalaire dépasse le seuil, les normales des triangles voisins seront interpolées.</span><span class="sxs-lookup"><span data-stu-id="cea2c-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-182">*ppMeshOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-183">Type : **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cea2c-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="cea2c-184">Adresse d’un pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) de sortie qui reçoit les données de vecteur tangente, Binormal et normal calculées.</span><span class="sxs-lookup"><span data-stu-id="cea2c-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-185">*ppVertexMapping* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-186">Type : **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cea2c-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="cea2c-187">Adresse d’un pointeur vers un objet de mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) de sortie qui reçoit un mappage de nouveaux vertex calculés par cette méthode aux vertex d’origine.</span><span class="sxs-lookup"><span data-stu-id="cea2c-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="cea2c-188">La mémoire tampon est un tableau de DWORDs, dont la taille de tableau est définie en tant que nombre de vertex dans ppMeshOut.</span><span class="sxs-lookup"><span data-stu-id="cea2c-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea2c-189">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cea2c-189">Return value</span></span>

<span data-ttu-id="cea2c-190">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cea2c-191">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cea2c-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cea2c-192">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cea2c-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea2c-193">Notes</span><span class="sxs-lookup"><span data-stu-id="cea2c-193">Remarks</span></span>

<span data-ttu-id="cea2c-194">Une version simplifiée de cette fonction est disponible en tant que [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span><span class="sxs-lookup"><span data-stu-id="cea2c-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="cea2c-195">Le vecteur normal calculé à chaque vertex est toujours normalisé pour avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="cea2c-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="cea2c-196">La solution la plus robuste pour calculer les coordonnées Cartésienles orthogonales consiste à ne pas définir d’indicateurs D3DXTANGENT \_ \_ de manière orthogonale à partir de \_ vous et D3DXTANGENT \_ à orthogonaliser \_ à partir de \_ v, afin que les coordonnées orthogonales soient calculées à partir des coordonnées de texture que vous et v.</span><span class="sxs-lookup"><span data-stu-id="cea2c-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="cea2c-197">Toutefois, dans ce cas, si u ou v est égal à zéro, la fonction calcule les coordonnées orthogonales à l’aide \_ de D3DXTANGENT orthogonale \_ de \_ v ou de D3DXTANGENT \_ orthogonale \_ à partir de \_ u, respectivement.</span><span class="sxs-lookup"><span data-stu-id="cea2c-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea2c-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cea2c-198">Requirements</span></span>



| <span data-ttu-id="cea2c-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cea2c-199">Requirement</span></span> | <span data-ttu-id="cea2c-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="cea2c-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea2c-201">En-tête</span><span class="sxs-lookup"><span data-stu-id="cea2c-201">Header</span></span><br/>  | <dl> <span data-ttu-id="cea2c-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea2c-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cea2c-203">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cea2c-203">Library</span></span><br/> | <dl> <span data-ttu-id="cea2c-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea2c-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cea2c-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cea2c-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea2c-206">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="cea2c-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="cea2c-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="cea2c-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
