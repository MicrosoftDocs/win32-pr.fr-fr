---
description: Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet :: GetSRT, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522993"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="20eff-103">ID3DXAnimationSet :: GetSRT, méthode</span><span class="sxs-lookup"><span data-stu-id="20eff-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="20eff-104">Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="20eff-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="20eff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20eff-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="20eff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20eff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20eff-107">*PeriodicPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20eff-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20eff-108">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20eff-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20eff-109">Position de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="20eff-109">Position of the animation set.</span></span> <span data-ttu-id="20eff-110">La position peut être obtenue en appelant [**ID3DXAnimationSet :: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span><span class="sxs-lookup"><span data-stu-id="20eff-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="20eff-111">*Animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20eff-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20eff-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20eff-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20eff-113">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="20eff-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="20eff-114">*pScale* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20eff-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20eff-115">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="20eff-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="20eff-116">Pointeur vers le vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit l’échelle de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="20eff-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="20eff-117">*protique* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20eff-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20eff-118">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="20eff-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="20eff-119">Pointeur vers le Quaternion [**D3DXQUATERNION**](d3dxquaternion.md) qui décrit la rotation de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="20eff-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="20eff-120">*pTranslation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20eff-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20eff-121">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="20eff-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="20eff-122">Pointeur vers le vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit la traduction de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="20eff-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20eff-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20eff-123">Return value</span></span>

<span data-ttu-id="20eff-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20eff-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20eff-125">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="20eff-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="20eff-126">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20eff-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="20eff-127">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="20eff-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20eff-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20eff-128">Requirements</span></span>



| <span data-ttu-id="20eff-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20eff-129">Requirement</span></span> | <span data-ttu-id="20eff-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="20eff-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20eff-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="20eff-131">Header</span></span><br/>  | <dl> <span data-ttu-id="20eff-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="20eff-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="20eff-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20eff-133">Library</span></span><br/> | <dl> <span data-ttu-id="20eff-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20eff-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20eff-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20eff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20eff-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="20eff-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
