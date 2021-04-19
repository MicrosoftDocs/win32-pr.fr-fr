---
description: Obtient la taille du carreau du rectangle.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: D3DXRectPatchSize, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532432"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="03e3a-103">D3DXRectPatchSize fonction)</span><span class="sxs-lookup"><span data-stu-id="03e3a-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="03e3a-104">Obtient la taille du carreau du rectangle.</span><span class="sxs-lookup"><span data-stu-id="03e3a-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03e3a-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="03e3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03e3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03e3a-107">*pfNumSegs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="03e3a-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03e3a-108">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="03e3a-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="03e3a-109">Nombre de segments par périphérie à paver.</span><span class="sxs-lookup"><span data-stu-id="03e3a-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="03e3a-110">*pdwTriangles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03e3a-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03e3a-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="03e3a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="03e3a-112">Pointeur vers une valeur DWORD qui contient le nombre de triangles dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="03e3a-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="03e3a-113">*pwdVertices* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03e3a-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03e3a-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="03e3a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="03e3a-115">Pointeur vers une valeur DWORD qui contient le nombre de vertex dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="03e3a-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03e3a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03e3a-116">Return value</span></span>

<span data-ttu-id="03e3a-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03e3a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03e3a-118">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="03e3a-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="03e3a-119">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="03e3a-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e3a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03e3a-120">Requirements</span></span>



| <span data-ttu-id="03e3a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03e3a-121">Requirement</span></span> | <span data-ttu-id="03e3a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="03e3a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03e3a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="03e3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="03e3a-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e3a-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="03e3a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03e3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="03e3a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03e3a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03e3a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03e3a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e3a-128">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="03e3a-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="03e3a-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="03e3a-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
