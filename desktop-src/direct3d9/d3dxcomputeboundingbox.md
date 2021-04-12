---
description: Calcule un cadre englobant orienté axe de coordonnées.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: D3DXComputeBoundingBox, fonction (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211803"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="b5c19-103">D3DXComputeBoundingBox, fonction (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="b5c19-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="b5c19-104">Calcule un cadre englobant orienté axe de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="b5c19-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5c19-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="b5c19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c19-107">*pFirstPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5c19-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c19-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5c19-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5c19-109">Pointeur vers la première position.</span><span class="sxs-lookup"><span data-stu-id="b5c19-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="b5c19-110">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5c19-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c19-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5c19-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5c19-112">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="b5c19-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b5c19-113">*dwStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5c19-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c19-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5c19-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5c19-115">Nombre ou nombre d’octets entre les vertex.</span><span class="sxs-lookup"><span data-stu-id="b5c19-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b5c19-116">*pMin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5c19-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c19-117">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5c19-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5c19-118">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle inférieur gauche retourné du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="b5c19-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="b5c19-119">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b5c19-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b5c19-120">*pMax* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b5c19-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c19-121">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5c19-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b5c19-122">Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle supérieur droit retourné du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="b5c19-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="b5c19-123">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b5c19-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c19-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5c19-124">Return value</span></span>

<span data-ttu-id="b5c19-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5c19-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5c19-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5c19-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5c19-127">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b5c19-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c19-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b5c19-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c19-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b5c19-129">Requirements</span></span>



| <span data-ttu-id="b5c19-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5c19-130">Requirement</span></span> | <span data-ttu-id="b5c19-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5c19-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c19-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5c19-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c19-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c19-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b5c19-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5c19-134">Library</span></span><br/> | <dl> <span data-ttu-id="b5c19-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5c19-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5c19-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5c19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c19-137">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b5c19-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
