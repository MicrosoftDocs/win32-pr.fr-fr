---
description: Retourne le Quaternion d’identité.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: D3DXQuaternionIdentity, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322834"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="45b7f-103">D3DXQuaternionIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="45b7f-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="45b7f-104">Retourne le Quaternion d’identité.</span><span class="sxs-lookup"><span data-stu-id="45b7f-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b7f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45b7f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="45b7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45b7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b7f-107">*moue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="45b7f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45b7f-108">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="45b7f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45b7f-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="45b7f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b7f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45b7f-110">Return value</span></span>

<span data-ttu-id="45b7f-111">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="45b7f-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45b7f-112">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui est le Quaternion d’identité.</span><span class="sxs-lookup"><span data-stu-id="45b7f-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b7f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="45b7f-113">Remarks</span></span>

<span data-ttu-id="45b7f-114">À partir d’un Quaternion (x, y, z, w), la fonction **D3DXQuaternionIdentity** retourne le Quaternion (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="45b7f-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="45b7f-115">La valeur de retour de cette fonction est la même que celle retournée dans le paramètre *moue* .</span><span class="sxs-lookup"><span data-stu-id="45b7f-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="45b7f-116">De cette façon, la fonction **D3DXQuaternionIdentity** peut être utilisée comme paramètre pour une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="45b7f-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="45b7f-117">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="45b7f-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b7f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45b7f-118">Requirements</span></span>



| <span data-ttu-id="45b7f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45b7f-119">Requirement</span></span> | <span data-ttu-id="45b7f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="45b7f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b7f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="45b7f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="45b7f-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b7f-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="45b7f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="45b7f-123">Library</span></span><br/> | <dl> <span data-ttu-id="45b7f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45b7f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45b7f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45b7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b7f-126">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="45b7f-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="45b7f-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="45b7f-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




