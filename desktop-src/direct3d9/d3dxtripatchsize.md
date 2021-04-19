---
description: Obtient la taille du correctif triangulaire.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: D3DXTriPatchSize, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ee254b12485153f4d5c5ba0843189399d1aed0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523183"
---
# <a name="d3dxtripatchsize-function"></a><span data-ttu-id="c9d8d-103">D3DXTriPatchSize fonction)</span><span class="sxs-lookup"><span data-stu-id="c9d8d-103">D3DXTriPatchSize function</span></span>

<span data-ttu-id="c9d8d-104">Obtient la taille du correctif triangulaire.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-104">Gets the size of the triangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d8d-105">Syntax</span></span>


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a><span data-ttu-id="c9d8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9d8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d8d-107">*pfNumSegs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9d8d-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d8d-108">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9d8d-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c9d8d-109">Nombre de segments par périphérie à paver.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="c9d8d-110">*pdwTriangles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9d8d-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d8d-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9d8d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c9d8d-112">Pointeur vers une valeur DWORD qui contient le nombre de triangles dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="c9d8d-113">*pdwVertices* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9d8d-113">*pdwVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d8d-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9d8d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c9d8d-115">Pointeur vers une valeur DWORD qui contient le nombre de vertex dans le correctif triangulaire.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-115">Pointer to a DWORD that contains the number of vertices in the triangle patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d8d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9d8d-116">Return value</span></span>

<span data-ttu-id="c9d8d-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9d8d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9d8d-118">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c9d8d-119">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c9d8d-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d8d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9d8d-120">Requirements</span></span>



| <span data-ttu-id="c9d8d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9d8d-121">Requirement</span></span> | <span data-ttu-id="c9d8d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d8d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d8d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9d8d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c9d8d-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d8d-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c9d8d-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9d8d-125">Library</span></span><br/> | <dl> <span data-ttu-id="c9d8d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9d8d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9d8d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d8d-128">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="c9d8d-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c9d8d-129">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="c9d8d-129">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
