---
description: Les soudures ensemble des vertex répliqués ayant des attributs identiques. Cette méthode utilise des valeurs epsilon spécifiées pour les comparaisons d’égalité.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: D3DXWeldVertices, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762085"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="64df4-104">D3DXWeldVertices fonction)</span><span class="sxs-lookup"><span data-stu-id="64df4-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="64df4-105">Les soudures ensemble des vertex répliqués ayant des attributs identiques.</span><span class="sxs-lookup"><span data-stu-id="64df4-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="64df4-106">Cette méthode utilise des valeurs epsilon spécifiées pour les comparaisons d’égalité.</span><span class="sxs-lookup"><span data-stu-id="64df4-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="64df4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64df4-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="64df4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64df4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64df4-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64df4-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="64df4-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="64df4-111">Pointeur vers un objet [**ID3DXMesh**](id3dxmesh.md) , le maillage à partir duquel les vertex de soudure.</span><span class="sxs-lookup"><span data-stu-id="64df4-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="64df4-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="64df4-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64df4-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64df4-114">Combinaison d’un ou plusieurs indicateurs à partir de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="64df4-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="64df4-115">*pEpsilons* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64df4-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-116">Type : **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="64df4-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="64df4-117">Pointeur vers une structure [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , en spécifiant les valeurs epsilon à utiliser pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="64df4-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="64df4-118">Utilisez **null** pour initialiser tous les membres de la structure avec une valeur par défaut de 1,0 e-6F.</span><span class="sxs-lookup"><span data-stu-id="64df4-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="64df4-119">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64df4-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-120">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="64df4-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="64df4-121">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage source.</span><span class="sxs-lookup"><span data-stu-id="64df4-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="64df4-122">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="64df4-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="64df4-123">Si ce paramètre a la valeur **null**, [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) est appelé pour créer des informations d’adjacence logiques.</span><span class="sxs-lookup"><span data-stu-id="64df4-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="64df4-124">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64df4-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="64df4-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="64df4-126">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="64df4-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="64df4-127">Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="64df4-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="64df4-128">*pFaceRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64df4-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-129">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="64df4-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="64df4-130">Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage soudé.</span><span class="sxs-lookup"><span data-stu-id="64df4-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="64df4-131">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64df4-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64df4-132">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64df4-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64df4-133">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="64df4-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="64df4-134">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="64df4-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64df4-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64df4-135">Return value</span></span>

<span data-ttu-id="64df4-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64df4-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64df4-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64df4-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64df4-138">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="64df4-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="64df4-139">Notes</span><span class="sxs-lookup"><span data-stu-id="64df4-139">Remarks</span></span>

<span data-ttu-id="64df4-140">Cette fonction utilise les informations d’adjacence fournies pour déterminer les points répliqués.</span><span class="sxs-lookup"><span data-stu-id="64df4-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="64df4-141">Les vertex sont fusionnés en fonction d’une comparaison Epsilon.</span><span class="sxs-lookup"><span data-stu-id="64df4-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="64df4-142">Les vertex avec la même position doivent déjà avoir été calculés et représentés par des données représentatives du point.</span><span class="sxs-lookup"><span data-stu-id="64df4-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="64df4-143">Cette fonction combine des vertex soudés logiquement qui ont des composants similaires, tels que des normales ou des coordonnées de texture dans pEpsilons.</span><span class="sxs-lookup"><span data-stu-id="64df4-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="64df4-144">L’exemple de code suivant appelle cette fonction avec le soudage activé.</span><span class="sxs-lookup"><span data-stu-id="64df4-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="64df4-145">Les vertex sont comparés à l’aide des valeurs epsilon pour le vecteur normal et la position du vertex.</span><span class="sxs-lookup"><span data-stu-id="64df4-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="64df4-146">Un pointeur est retourné à un tableau de remappages de visages (*pFaceRemap*).</span><span class="sxs-lookup"><span data-stu-id="64df4-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="64df4-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64df4-147">Requirements</span></span>



| <span data-ttu-id="64df4-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64df4-148">Requirement</span></span> | <span data-ttu-id="64df4-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="64df4-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64df4-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="64df4-150">Header</span></span><br/>  | <dl> <span data-ttu-id="64df4-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="64df4-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="64df4-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64df4-152">Library</span></span><br/> | <dl> <span data-ttu-id="64df4-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64df4-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64df4-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64df4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64df4-155">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="64df4-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
