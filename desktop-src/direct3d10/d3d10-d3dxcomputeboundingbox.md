---
description: 'Fonction D3DXComputeBoundingBox (D3DX10math. h) : calcule un cadre englobant orienté axe de coordonnées.'
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: D3DXComputeBoundingBox, fonction (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103527"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="4c863-103">D3DXComputeBoundingBox, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="4c863-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="4c863-104">Calcule un cadre englobant orienté axe de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="4c863-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c863-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c863-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="4c863-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c863-107">*pFirstPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c863-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c863-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c863-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c863-109">Pointeur vers la première position.</span><span class="sxs-lookup"><span data-stu-id="4c863-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="4c863-110">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c863-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c863-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c863-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c863-112">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="4c863-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4c863-113">*dwStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c863-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c863-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c863-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c863-115">Nombre ou nombre d’octets entre les vertex.</span><span class="sxs-lookup"><span data-stu-id="4c863-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4c863-116">*pMin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c863-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c863-117">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c863-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c863-118">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle inférieur gauche retourné du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="4c863-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="4c863-119">*pMax* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4c863-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c863-120">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c863-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c863-121">Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle supérieur droit retourné du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="4c863-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c863-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c863-122">Return value</span></span>

<span data-ttu-id="4c863-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c863-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c863-124">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c863-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c863-125">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4c863-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c863-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c863-126">Requirements</span></span>



| <span data-ttu-id="4c863-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c863-127">Requirement</span></span> | <span data-ttu-id="4c863-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c863-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c863-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c863-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4c863-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c863-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c863-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c863-131">Library</span></span><br/> | <dl> <span data-ttu-id="4c863-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c863-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c863-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c863-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c863-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="4c863-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
