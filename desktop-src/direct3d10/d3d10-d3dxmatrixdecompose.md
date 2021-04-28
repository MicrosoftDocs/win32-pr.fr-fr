---
description: 'Fonction D3DXMatrixDecompose (D3DX10Math. h) : décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.'
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
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113207"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="34a1f-103">D3DXMatrixDecompose, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="34a1f-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="34a1f-104">Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.</span><span class="sxs-lookup"><span data-stu-id="34a1f-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34a1f-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="34a1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a1f-107">*pOutScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34a1f-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a1f-108">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a1f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34a1f-109">Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) de sortie qui contient les facteurs d’échelle appliqués le long des axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="34a1f-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="34a1f-110">*pOutRotation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34a1f-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a1f-111">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a1f-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="34a1f-112">Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui décrit la rotation.</span><span class="sxs-lookup"><span data-stu-id="34a1f-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="34a1f-113">*pOutTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34a1f-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a1f-114">Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a1f-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34a1f-115">Pointeur vers le vecteur D3DXVECTOR3 qui décrit la traduction.</span><span class="sxs-lookup"><span data-stu-id="34a1f-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="34a1f-116">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34a1f-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a1f-117">Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a1f-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="34a1f-118">Pointeur vers une matrice d’entrée [**D3DXMATRIX**](d3d10-d3dxmatrix.md) à décomposer.</span><span class="sxs-lookup"><span data-stu-id="34a1f-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a1f-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34a1f-119">Return value</span></span>

<span data-ttu-id="34a1f-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34a1f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34a1f-121">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34a1f-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="34a1f-122">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="34a1f-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a1f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34a1f-123">Requirements</span></span>



| <span data-ttu-id="34a1f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34a1f-124">Requirement</span></span> | <span data-ttu-id="34a1f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a1f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a1f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="34a1f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="34a1f-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a1f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="34a1f-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34a1f-128">Library</span></span><br/> | <dl> <span data-ttu-id="34a1f-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a1f-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34a1f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34a1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a1f-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="34a1f-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
