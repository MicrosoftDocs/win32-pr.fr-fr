---
description: Retourne le produit scalaire de deux quaternions.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: D3DXQuaternionDot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323185"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="05d23-103">D3DXQuaternionDot fonction)</span><span class="sxs-lookup"><span data-stu-id="05d23-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="05d23-104">Retourne le produit scalaire de deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="05d23-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d23-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05d23-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="05d23-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05d23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d23-107">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05d23-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d23-108">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="05d23-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="05d23-109">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="05d23-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="05d23-110">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05d23-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d23-111">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="05d23-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="05d23-112">Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.</span><span class="sxs-lookup"><span data-stu-id="05d23-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d23-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05d23-113">Return value</span></span>

<span data-ttu-id="05d23-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05d23-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05d23-115">Produit scalaire de deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="05d23-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d23-116">Notes</span><span class="sxs-lookup"><span data-stu-id="05d23-116">Remarks</span></span>

<span data-ttu-id="05d23-117">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="05d23-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d23-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05d23-118">Requirements</span></span>



| <span data-ttu-id="05d23-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05d23-119">Requirement</span></span> | <span data-ttu-id="05d23-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05d23-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05d23-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="05d23-121">Header</span></span><br/>  | <dl> <span data-ttu-id="05d23-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="05d23-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="05d23-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05d23-123">Library</span></span><br/> | <dl> <span data-ttu-id="05d23-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05d23-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05d23-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05d23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d23-126">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="05d23-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
