---
description: Calcule une sphère englobante pour la maille.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: D3DXComputeBoundingSphere, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9e6a0c9fb67abe8a98ccf8b3f9b895fd63fc3e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535183"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="dcebb-103">D3DXComputeBoundingSphere, fonction (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="dcebb-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="dcebb-104">Calcule une sphère englobante pour la maille.</span><span class="sxs-lookup"><span data-stu-id="dcebb-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcebb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcebb-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="dcebb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcebb-107">*pFirstPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcebb-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcebb-108">Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcebb-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dcebb-109">Pointeur vers la première position.</span><span class="sxs-lookup"><span data-stu-id="dcebb-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="dcebb-110">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcebb-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcebb-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcebb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcebb-112">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="dcebb-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="dcebb-113">*dwStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcebb-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcebb-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcebb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcebb-115">Nombre d’octets entre les vecteurs de position.</span><span class="sxs-lookup"><span data-stu-id="dcebb-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="dcebb-116">Utilisez [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)ou [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) pour accéder au Stride du vertex.</span><span class="sxs-lookup"><span data-stu-id="dcebb-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="dcebb-117">*pCenter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcebb-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcebb-118">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcebb-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dcebb-119">Structure [**D3DXVECTOR3**](d3dxvector3.md) , qui définit le centre de coordonnées de la sphère englobante retournée.</span><span class="sxs-lookup"><span data-stu-id="dcebb-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="dcebb-120">*pRadius* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcebb-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcebb-121">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcebb-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dcebb-122">Rayon de la sphère englobante retournée.</span><span class="sxs-lookup"><span data-stu-id="dcebb-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcebb-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcebb-123">Return value</span></span>

<span data-ttu-id="dcebb-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcebb-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcebb-125">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcebb-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcebb-126">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dcebb-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcebb-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcebb-127">Requirements</span></span>



| <span data-ttu-id="dcebb-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcebb-128">Requirement</span></span> | <span data-ttu-id="dcebb-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcebb-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcebb-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcebb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dcebb-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcebb-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dcebb-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcebb-132">Library</span></span><br/> | <dl> <span data-ttu-id="dcebb-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcebb-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dcebb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcebb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcebb-135">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="dcebb-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
