---
description: Créez un pool d’effets. Un pool est utilisé pour partager des paramètres entre les effets.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: D3DXCreateEffectPool, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211916"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="c8fdc-104">D3DXCreateEffectPool fonction)</span><span class="sxs-lookup"><span data-stu-id="c8fdc-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="c8fdc-105">Créez un pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-105">Create an effect pool.</span></span> <span data-ttu-id="c8fdc-106">Un pool est utilisé pour partager des paramètres entre les effets.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8fdc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8fdc-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="c8fdc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8fdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8fdc-109">*ppPool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c8fdc-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8fdc-110">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8fdc-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="c8fdc-111">Retourne un pointeur vers le pool créé.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8fdc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8fdc-112">Return value</span></span>

<span data-ttu-id="c8fdc-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8fdc-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8fdc-114">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="c8fdc-115">Si les arguments ne sont pas valides, la méthode retourne D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c8fdc-116">Si la méthode échoue, la valeur de retour est E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8fdc-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c8fdc-117">Remarks</span></span>

<span data-ttu-id="c8fdc-118">Pour les effets au sein d’un pool, les paramètres partagés portant le même nom partagent des valeurs.</span><span class="sxs-lookup"><span data-stu-id="c8fdc-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8fdc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8fdc-119">Requirements</span></span>



| <span data-ttu-id="c8fdc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8fdc-120">Requirement</span></span> | <span data-ttu-id="c8fdc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8fdc-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fdc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8fdc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c8fdc-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8fdc-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c8fdc-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8fdc-124">Library</span></span><br/> | <dl> <span data-ttu-id="c8fdc-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8fdc-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c8fdc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8fdc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8fdc-127">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="c8fdc-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




