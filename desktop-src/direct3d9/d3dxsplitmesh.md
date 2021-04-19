---
description: Divise un maillage en maillages plus petits que la taille spécifiée.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: D3DXSplitMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535809"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="a31fe-103">D3DXSplitMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="a31fe-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="a31fe-104">Divise un maillage en maillages plus petits que la taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a31fe-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a31fe-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="a31fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a31fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a31fe-107">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a31fe-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a31fe-109">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant la maille source.</span><span class="sxs-lookup"><span data-stu-id="a31fe-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-110">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-111">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a31fe-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a31fe-112">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille à simplifier.</span><span class="sxs-lookup"><span data-stu-id="a31fe-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-113">*MaxSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-114">Type : **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a31fe-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a31fe-115">Nombre maximal de vertex dans le maillage résultant.</span><span class="sxs-lookup"><span data-stu-id="a31fe-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-116">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-117">Type : **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a31fe-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a31fe-118">Indicateurs d’option pour les nouveaux maillages.</span><span class="sxs-lookup"><span data-stu-id="a31fe-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-119">*pMeshesOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a31fe-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a31fe-121">Nombre de maillages retournés.</span><span class="sxs-lookup"><span data-stu-id="a31fe-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-122">*ppMeshArrayOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-123">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a31fe-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a31fe-124">Mémoire tampon contenant un tableau d’interfaces [**ID3DXMesh**](id3dxmesh.md) pour les nouveaux maillages.</span><span class="sxs-lookup"><span data-stu-id="a31fe-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="a31fe-125">Pour un maillage source divisé en n maillages, *ppMeshArrayOut* est un tableau de n pointeurs **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="a31fe-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-126">*ppAdjacencyArrayOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-127">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a31fe-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a31fe-128">Mémoire tampon contenant un tableau de tableaux d’adjacence (DWORDs) pour les nouveaux maillages.</span><span class="sxs-lookup"><span data-stu-id="a31fe-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="a31fe-129">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a31fe-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="a31fe-130">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a31fe-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-131">*ppFaceRemapArrayOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-132">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a31fe-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a31fe-133">Mémoire tampon contenant un tableau de tableaux de remappages de visages (DWORDs) pour les nouveaux maillages.</span><span class="sxs-lookup"><span data-stu-id="a31fe-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="a31fe-134">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a31fe-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="a31fe-135">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a31fe-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a31fe-136">*ppVertRemapArrayOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fe-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fe-137">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a31fe-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a31fe-138">Mémoire tampon contenant un tableau de tableaux de remappage de vertex pour les nouveaux maillages.</span><span class="sxs-lookup"><span data-stu-id="a31fe-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="a31fe-139">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a31fe-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="a31fe-140">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a31fe-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31fe-141">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a31fe-141">Return value</span></span>

<span data-ttu-id="a31fe-142">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a31fe-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a31fe-143">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a31fe-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a31fe-144">Notes</span><span class="sxs-lookup"><span data-stu-id="a31fe-144">Remarks</span></span>

<span data-ttu-id="a31fe-145">Cette fonction est couramment utilisée pour fractionner un maillage avec des index 32 bits (plus de 65535 sommets) en plusieurs maillages, chacun ayant des index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a31fe-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="a31fe-146">Les tableaux d’adjacence, de remappage de sommets et de remappage de face sont des tableaux de type DWORD, où chaque tableau contient n pointeurs DWORD, suivis des données DWORD référencées par les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="a31fe-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="a31fe-147">Par exemple, pour obtenir les informations de remappage de visage pour la face 3 de la maille 2, vous pouvez utiliser le code suivant, en supposant que les données de remappage de face ont été retournées dans une variable nommée *ppFaceRemapArrayOut*.</span><span class="sxs-lookup"><span data-stu-id="a31fe-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="a31fe-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a31fe-148">Requirements</span></span>



| <span data-ttu-id="a31fe-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a31fe-149">Requirement</span></span> | <span data-ttu-id="a31fe-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="a31fe-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a31fe-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="a31fe-151">Header</span></span><br/>  | <dl> <span data-ttu-id="a31fe-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a31fe-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a31fe-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a31fe-153">Library</span></span><br/> | <dl> <span data-ttu-id="a31fe-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a31fe-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a31fe-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a31fe-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31fe-156">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="a31fe-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
