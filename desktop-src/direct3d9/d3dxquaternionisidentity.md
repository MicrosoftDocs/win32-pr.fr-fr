---
description: Détermine si un Quaternion est un Quaternion d’identité.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: D3DXQuaternionIsIdentity, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106541258"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="fecb3-103">D3DXQuaternionIsIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="fecb3-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="fecb3-104">Détermine si un Quaternion est un Quaternion d’identité.</span><span class="sxs-lookup"><span data-stu-id="fecb3-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="fecb3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fecb3-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="fecb3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fecb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fecb3-107">*PQ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fecb3-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fecb3-108">Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fecb3-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fecb3-109">Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) qui sera testée pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="fecb3-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fecb3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fecb3-110">Return value</span></span>

<span data-ttu-id="fecb3-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fecb3-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fecb3-112">Si le Quaternion est un Quaternion d’identité, cette fonction retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="fecb3-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="fecb3-113">Dans le cas contraire, cette fonction retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fecb3-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fecb3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fecb3-114">Remarks</span></span>

<span data-ttu-id="fecb3-115">Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="fecb3-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fecb3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fecb3-116">Requirements</span></span>



| <span data-ttu-id="fecb3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fecb3-117">Requirement</span></span> | <span data-ttu-id="fecb3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fecb3-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fecb3-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="fecb3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fecb3-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fecb3-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fecb3-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fecb3-121">Library</span></span><br/> | <dl> <span data-ttu-id="fecb3-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fecb3-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fecb3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fecb3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecb3-124">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="fecb3-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fecb3-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="fecb3-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
