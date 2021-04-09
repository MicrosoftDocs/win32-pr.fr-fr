---
description: Calcule les normales des unités pour chaque vertex d’une maille. Fourni pour prendre en charge les applications héritées. Utilisez D3DXComputeTangentFrameEx pour obtenir de meilleurs résultats.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: D3DXComputeNormals, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953902"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="9d57e-105">D3DXComputeNormals fonction)</span><span class="sxs-lookup"><span data-stu-id="9d57e-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="9d57e-106">Calcule les normales des unités pour chaque vertex d’une maille.</span><span class="sxs-lookup"><span data-stu-id="9d57e-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="9d57e-107">Fourni pour prendre en charge les applications héritées.</span><span class="sxs-lookup"><span data-stu-id="9d57e-107">Provided to support legacy applications.</span></span> <span data-ttu-id="9d57e-108">Utilisez [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) pour obtenir de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="9d57e-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d57e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d57e-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="9d57e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d57e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d57e-111">*pMesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9d57e-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d57e-112">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9d57e-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="9d57e-113">Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant l’objet de maillage normalisé.</span><span class="sxs-lookup"><span data-stu-id="9d57e-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="9d57e-114">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d57e-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d57e-115">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d57e-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d57e-116">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans la maille progressive créée.</span><span class="sxs-lookup"><span data-stu-id="9d57e-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="9d57e-117">Ce paramètre est facultatif et doit avoir la valeur **null** s’il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d57e-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d57e-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d57e-118">Return value</span></span>

<span data-ttu-id="9d57e-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d57e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d57e-120">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9d57e-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9d57e-121">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9d57e-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d57e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="9d57e-122">Remarks</span></span>

<span data-ttu-id="9d57e-123">Le maillage d’entrée doit avoir l’indicateur [ \_ normal D3DFVF](d3dfvf.md) spécifié dans son format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="9d57e-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="9d57e-124">Un normal pour un vertex est généré en calculant la moyenne des normales de tous les visages qui partagent ce vertex.</span><span class="sxs-lookup"><span data-stu-id="9d57e-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="9d57e-125">Si une contiguïté est fournie, les vertex répliqués sont ignorés et « lissés » sur.</span><span class="sxs-lookup"><span data-stu-id="9d57e-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="9d57e-126">Si l’adjacence n’est pas fournie, les vertex répliqués auront des normales dont la moyenne est calculée à partir de uniquement les visages qui les référencent explicitement.</span><span class="sxs-lookup"><span data-stu-id="9d57e-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="9d57e-127">Cette fonction appelle simplement [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) avec les paramètres d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="9d57e-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="9d57e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d57e-128">Requirements</span></span>



| <span data-ttu-id="9d57e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d57e-129">Requirement</span></span> | <span data-ttu-id="9d57e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d57e-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d57e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d57e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9d57e-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d57e-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9d57e-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d57e-133">Library</span></span><br/> | <dl> <span data-ttu-id="9d57e-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d57e-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d57e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d57e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d57e-136">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="9d57e-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
