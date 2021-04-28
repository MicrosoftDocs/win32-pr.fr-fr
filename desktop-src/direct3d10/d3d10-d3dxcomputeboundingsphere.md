---
description: 'Fonction D3DXComputeBoundingSphere (D3DX10math. h) : calcule une sphère englobante pour la maille.'
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: D3DXComputeBoundingSphere, fonction (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113297"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="b68cc-103">D3DXComputeBoundingSphere, fonction (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="b68cc-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="b68cc-104">Calcule une sphère englobante pour la maille.</span><span class="sxs-lookup"><span data-stu-id="b68cc-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b68cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b68cc-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="b68cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b68cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b68cc-107">*pFirstPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b68cc-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68cc-108">Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b68cc-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b68cc-109">Pointeur vers la première position.</span><span class="sxs-lookup"><span data-stu-id="b68cc-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="b68cc-110">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b68cc-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68cc-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b68cc-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b68cc-112">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="b68cc-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b68cc-113">*dwStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b68cc-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68cc-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b68cc-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b68cc-115">Nombre d’octets entre les vecteurs de position.</span><span class="sxs-lookup"><span data-stu-id="b68cc-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="b68cc-116">*pCenter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b68cc-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68cc-117">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b68cc-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b68cc-118">Structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , qui définit le centre de coordonnées de la sphère englobante retournée.</span><span class="sxs-lookup"><span data-stu-id="b68cc-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="b68cc-119">*pRadius* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b68cc-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68cc-120">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b68cc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b68cc-121">Rayon de la sphère englobante retournée.</span><span class="sxs-lookup"><span data-stu-id="b68cc-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b68cc-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b68cc-122">Return value</span></span>

<span data-ttu-id="b68cc-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b68cc-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b68cc-124">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b68cc-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b68cc-125">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b68cc-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b68cc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b68cc-126">Requirements</span></span>



| <span data-ttu-id="b68cc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b68cc-127">Requirement</span></span> | <span data-ttu-id="b68cc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b68cc-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b68cc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b68cc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b68cc-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b68cc-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="b68cc-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b68cc-131">Library</span></span><br/> | <dl> <span data-ttu-id="b68cc-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b68cc-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b68cc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b68cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68cc-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b68cc-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
