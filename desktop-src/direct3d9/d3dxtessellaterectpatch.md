---
description: Tessellates un carreau rectangulaire de surface d’ordre supérieur dans un maillage de triangle.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: D3DXTessellateRectPatch, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211741"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="1192d-103">D3DXTessellateRectPatch fonction)</span><span class="sxs-lookup"><span data-stu-id="1192d-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="1192d-104">Tessellates un carreau rectangulaire de surface d’ordre supérieur dans un maillage de triangle.</span><span class="sxs-lookup"><span data-stu-id="1192d-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1192d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1192d-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1192d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1192d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1192d-107">*pVB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1192d-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1192d-108">Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="1192d-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="1192d-109">Mémoire tampon de vertex contenant les données de correctif.</span><span class="sxs-lookup"><span data-stu-id="1192d-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="1192d-110">*pNumSegs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1192d-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1192d-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1192d-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1192d-112">Pointeur vers un tableau de quatre valeurs à virgule flottante qui identifient le nombre de segments dans lequel chaque bord du correctif de rectangle doit être divisé lorsqu’il est fractionné.</span><span class="sxs-lookup"><span data-stu-id="1192d-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="1192d-113">Consultez [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="1192d-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="1192d-114">*pInDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1192d-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1192d-115">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1192d-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="1192d-116">Structure de déclaration de vertex qui définit les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="1192d-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="1192d-117">Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="1192d-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="1192d-118">*pRectPatchInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1192d-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1192d-119">Type : **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="1192d-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="1192d-120">Décrit un correctif rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="1192d-120">Describes a rectangular patch.</span></span> <span data-ttu-id="1192d-121">Consultez [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="1192d-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="1192d-122">*pMesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1192d-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1192d-123">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1192d-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1192d-124">Pointeur vers le maillage créé.</span><span class="sxs-lookup"><span data-stu-id="1192d-124">Pointer to the created mesh.</span></span> <span data-ttu-id="1192d-125">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="1192d-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1192d-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1192d-126">Return value</span></span>

<span data-ttu-id="1192d-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1192d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1192d-128">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1192d-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1192d-129">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1192d-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1192d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1192d-130">Remarks</span></span>

<span data-ttu-id="1192d-131">Utilisez [**D3DXRectPatchSize**](d3dxrectpatchsize.md) pour connaître le nombre de vertex et d’index de sortie dont la fonction de pavage a besoin.</span><span class="sxs-lookup"><span data-stu-id="1192d-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1192d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1192d-132">Requirements</span></span>



| <span data-ttu-id="1192d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1192d-133">Requirement</span></span> | <span data-ttu-id="1192d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1192d-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1192d-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1192d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1192d-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1192d-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1192d-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1192d-137">Library</span></span><br/> | <dl> <span data-ttu-id="1192d-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1192d-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1192d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1192d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1192d-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="1192d-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1192d-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="1192d-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
