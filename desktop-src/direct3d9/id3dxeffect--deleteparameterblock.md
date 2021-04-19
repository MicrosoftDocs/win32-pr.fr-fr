---
description: Supprimer un bloc de paramètres.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: ID3DXEffect ::D méthode eleteParameterBlock (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531782"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="0d5a5-103">ID3DXEffect ::D méthode eleteParameterBlock</span><span class="sxs-lookup"><span data-stu-id="0d5a5-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="0d5a5-104">Supprimer un bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d5a5-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="0d5a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d5a5-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="0d5a5-107">*hParameterBlock* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d5a5-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5a5-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0d5a5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0d5a5-109">Handle du bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-109">A handle to the parameter block.</span></span> <span data-ttu-id="0d5a5-110">Il s’agit du handle retourné par [**ID3DXEffect :: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="0d5a5-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d5a5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d5a5-111">Return value</span></span>

<span data-ttu-id="0d5a5-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d5a5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d5a5-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d5a5-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5a5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0d5a5-115">Remarks</span></span>

<span data-ttu-id="0d5a5-116">Les blocs de paramètres sont des blocs d’États d’effet.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="0d5a5-117">Utilisez un bloc de paramètres pour enregistrer les modifications d’État afin qu’elles puissent être appliquées ultérieurement avec un seul appel d’API.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="0d5a5-118">Quand vous n’en avez plus besoin, supprimez le bloc de paramètres pour réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0d5a5-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5a5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d5a5-119">Requirements</span></span>



| <span data-ttu-id="0d5a5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d5a5-120">Requirement</span></span> | <span data-ttu-id="0d5a5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d5a5-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5a5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d5a5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0d5a5-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a5-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0d5a5-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d5a5-124">Library</span></span><br/> | <dl> <span data-ttu-id="0d5a5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d5a5-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d5a5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d5a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5a5-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="0d5a5-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="0d5a5-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="0d5a5-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="0d5a5-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="0d5a5-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




