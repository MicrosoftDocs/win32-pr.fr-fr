---
description: Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: D3DXMatrixDecompose, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211913"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="31139-103">D3DXMatrixDecompose, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="31139-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="31139-104">Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.</span><span class="sxs-lookup"><span data-stu-id="31139-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="31139-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31139-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="31139-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31139-107">*pOutScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31139-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31139-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="31139-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="31139-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) de sortie qui contient les facteurs d’échelle appliqués le long des axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="31139-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="31139-110">*pOutRotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31139-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31139-111">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="31139-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="31139-112">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui décrit la rotation.</span><span class="sxs-lookup"><span data-stu-id="31139-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="31139-113">*pOutTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31139-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31139-114">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="31139-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="31139-115">Pointeur vers le vecteur D3DXVECTOR3 qui décrit la traduction.</span><span class="sxs-lookup"><span data-stu-id="31139-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="31139-116">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31139-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31139-117">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="31139-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31139-118">Pointeur vers une matrice d’entrée [**D3DXMATRIX**](d3d10-d3dxmatrix.md) à décomposer.</span><span class="sxs-lookup"><span data-stu-id="31139-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31139-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31139-119">Return value</span></span>

<span data-ttu-id="31139-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31139-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31139-121">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31139-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="31139-122">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="31139-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="31139-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31139-123">Requirements</span></span>



| <span data-ttu-id="31139-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31139-124">Requirement</span></span> | <span data-ttu-id="31139-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="31139-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31139-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="31139-126">Header</span></span><br/>  | <dl> <span data-ttu-id="31139-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="31139-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="31139-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31139-128">Library</span></span><br/> | <dl> <span data-ttu-id="31139-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31139-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31139-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31139-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31139-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="31139-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
