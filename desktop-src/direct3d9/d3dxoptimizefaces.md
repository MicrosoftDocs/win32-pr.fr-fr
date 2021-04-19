---
description: Génère un remappage de visage optimisé pour une liste de triangles.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: D3DXOptimizeFaces, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538967"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="f6417-103">D3DXOptimizeFaces fonction)</span><span class="sxs-lookup"><span data-stu-id="f6417-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="f6417-104">Génère un remappage de visage optimisé pour une liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="f6417-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6417-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6417-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="f6417-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6417-107">*pIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6417-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6417-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6417-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6417-109">Pointeur vers les index de liste de triangles à utiliser pour trier les vertex.</span><span class="sxs-lookup"><span data-stu-id="f6417-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="f6417-110">*NumFaces* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6417-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6417-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6417-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6417-112">Nombre de visages dans la liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="f6417-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="f6417-113">Pour les maillages 16 bits, cette valeur est limitée à 2 ^ 16-1 (65535) ou moins de visages.</span><span class="sxs-lookup"><span data-stu-id="f6417-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="f6417-114">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6417-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6417-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6417-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6417-116">Nombre de vertex référencés par la liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="f6417-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="f6417-117">*Indices32Bit* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6417-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6417-118">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6417-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6417-119">Indicateur qui spécifie le type d’index : **true** si les index sont 32 bits (plus de 65535 index), **false** si les index sont 16 bits (65535 ou moins d’index).</span><span class="sxs-lookup"><span data-stu-id="f6417-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="f6417-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f6417-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6417-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6417-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f6417-122">Pointeur vers la face de maille d’origine qui a été fractionnée pour générer la face actuelle.</span><span class="sxs-lookup"><span data-stu-id="f6417-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6417-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6417-123">Return value</span></span>

<span data-ttu-id="f6417-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6417-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6417-125">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6417-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f6417-126">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f6417-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6417-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f6417-127">Remarks</span></span>

<span data-ttu-id="f6417-128">La procédure d’optimisation de cette fonction est fonctionnellement équivalente à l’appel de [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) avec l' \_ indicateur D3DXMESHOPT DEVICEINDEPENDENT, mais cette fonction permet une utilisation plus efficace des caches de vertex.</span><span class="sxs-lookup"><span data-stu-id="f6417-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6417-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6417-129">Requirements</span></span>



| <span data-ttu-id="f6417-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6417-130">Requirement</span></span> | <span data-ttu-id="f6417-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6417-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6417-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6417-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f6417-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6417-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f6417-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6417-134">Library</span></span><br/> | <dl> <span data-ttu-id="f6417-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6417-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6417-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6417-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6417-137">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="f6417-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
