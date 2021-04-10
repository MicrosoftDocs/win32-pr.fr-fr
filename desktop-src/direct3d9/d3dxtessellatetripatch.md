---
description: Tessellates un carreau de surface d’ordre supérieur triangulaire dans un maillage de triangles.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: D3DXTessellateTriPatch, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762019"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="04e9c-103">D3DXTessellateTriPatch fonction)</span><span class="sxs-lookup"><span data-stu-id="04e9c-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="04e9c-104">Tessellates un carreau de surface d’ordre supérieur triangulaire dans un maillage de triangles.</span><span class="sxs-lookup"><span data-stu-id="04e9c-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04e9c-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="04e9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04e9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e9c-107">*pVB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e9c-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e9c-108">Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="04e9c-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="04e9c-109">Mémoire tampon de vertex contenant les données de correctif.</span><span class="sxs-lookup"><span data-stu-id="04e9c-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="04e9c-110">*pNumSegs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e9c-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e9c-111">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="04e9c-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04e9c-112">Pointeur vers un tableau de trois valeurs à virgule flottante qui identifient le nombre de segments dans lequel chaque bord du correctif triangulaire doit être divisé lorsqu’il est fractionné.</span><span class="sxs-lookup"><span data-stu-id="04e9c-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="04e9c-113">Consultez [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="04e9c-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="04e9c-114">*pInDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e9c-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e9c-115">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="04e9c-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="04e9c-116">Structure de déclaration de vertex qui définit les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="04e9c-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="04e9c-117">Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="04e9c-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="04e9c-118">*pTriPatchInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e9c-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e9c-119">Type : **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="04e9c-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="04e9c-120">Décrit un correctif triangulaire.</span><span class="sxs-lookup"><span data-stu-id="04e9c-120">Describes a triangle patch.</span></span> <span data-ttu-id="04e9c-121">Consultez [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="04e9c-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="04e9c-122">*pMesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="04e9c-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e9c-123">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="04e9c-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="04e9c-124">Pointeur vers le maillage créé.</span><span class="sxs-lookup"><span data-stu-id="04e9c-124">Pointer to the created mesh.</span></span> <span data-ttu-id="04e9c-125">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="04e9c-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e9c-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04e9c-126">Return value</span></span>

<span data-ttu-id="04e9c-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04e9c-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04e9c-128">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04e9c-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04e9c-129">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="04e9c-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e9c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="04e9c-130">Remarks</span></span>

<span data-ttu-id="04e9c-131">Utilisez [**D3DXTriPatchSize**](d3dxtripatchsize.md) pour connaître le nombre de vertex et d’index de sortie dont la fonction de pavage a besoin.</span><span class="sxs-lookup"><span data-stu-id="04e9c-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e9c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04e9c-132">Requirements</span></span>



| <span data-ttu-id="04e9c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04e9c-133">Requirement</span></span> | <span data-ttu-id="04e9c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="04e9c-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04e9c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="04e9c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="04e9c-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e9c-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="04e9c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04e9c-137">Library</span></span><br/> | <dl> <span data-ttu-id="04e9c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04e9c-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04e9c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e9c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e9c-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="04e9c-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="04e9c-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="04e9c-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
