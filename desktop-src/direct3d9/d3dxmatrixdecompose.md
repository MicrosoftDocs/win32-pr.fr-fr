---
description: Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: D3DXMatrixDecompose, fonction (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539908"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="a8b54-103">D3DXMatrixDecompose, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a8b54-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="a8b54-104">Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.</span><span class="sxs-lookup"><span data-stu-id="a8b54-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b54-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8b54-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a8b54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8b54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b54-107">*pOutScale* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a8b54-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b54-108">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8b54-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a8b54-109">Pointeur vers le [**D3DXVECTOR3**](d3dxvector3.md) de sortie qui contient les facteurs d’échelle appliqués le long des axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="a8b54-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="a8b54-110">*pOutRotation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a8b54-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b54-111">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8b54-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a8b54-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui décrit la rotation.</span><span class="sxs-lookup"><span data-stu-id="a8b54-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="a8b54-113">*pOutTranslation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a8b54-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b54-114">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8b54-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a8b54-115">Pointeur vers le vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit la traduction.</span><span class="sxs-lookup"><span data-stu-id="a8b54-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="a8b54-116">*GCF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8b54-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b54-117">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8b54-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8b54-118">Pointeur vers une matrice d’entrée [**D3DXMATRIX**](d3dxmatrix.md) à décomposer.</span><span class="sxs-lookup"><span data-stu-id="a8b54-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b54-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8b54-119">Return value</span></span>

<span data-ttu-id="a8b54-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8b54-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8b54-121">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8b54-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a8b54-122">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a8b54-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b54-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8b54-123">Requirements</span></span>



| <span data-ttu-id="a8b54-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8b54-124">Requirement</span></span> | <span data-ttu-id="a8b54-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8b54-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b54-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8b54-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b54-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b54-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8b54-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8b54-128">Library</span></span><br/> | <dl> <span data-ttu-id="a8b54-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8b54-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8b54-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8b54-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b54-131">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="a8b54-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




