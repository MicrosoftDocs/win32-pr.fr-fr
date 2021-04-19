---
description: Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect :: ApplyParameterBlock, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531341"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="226b9-103">ID3DXEffect :: ApplyParameterBlock, méthode</span><span class="sxs-lookup"><span data-stu-id="226b9-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="226b9-104">Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.</span><span class="sxs-lookup"><span data-stu-id="226b9-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="226b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="226b9-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="226b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="226b9-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="226b9-107">*hParameterBlock* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="226b9-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="226b9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="226b9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="226b9-109">Handle du bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="226b9-109">A handle to the parameter block.</span></span> <span data-ttu-id="226b9-110">Il s’agit du handle retourné par [**ID3DXEffect :: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="226b9-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="226b9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="226b9-111">Return value</span></span>

<span data-ttu-id="226b9-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="226b9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="226b9-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="226b9-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="226b9-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="226b9-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="226b9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="226b9-115">Remarks</span></span>

<span data-ttu-id="226b9-116">L’état du paramètre d’effet de capture change dans un bloc de paramètres en appelant BeginParameterBlock ; Arrêtez la capture des modifications d’État en appelant EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="226b9-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="226b9-117">Ces modifications d’État incluent les modifications de paramètres d’effet qui se produisent à l’intérieur d’une technique (y compris celles en dehors d’une passe).</span><span class="sxs-lookup"><span data-stu-id="226b9-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="226b9-118">Une fois que vous avez terminé avec le bloc de paramètres, appelez DeleteParameterBlock pour récupérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="226b9-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="226b9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="226b9-119">Requirements</span></span>



| <span data-ttu-id="226b9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="226b9-120">Requirement</span></span> | <span data-ttu-id="226b9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="226b9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="226b9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="226b9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="226b9-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="226b9-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="226b9-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="226b9-124">Library</span></span><br/> | <dl> <span data-ttu-id="226b9-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="226b9-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="226b9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="226b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226b9-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="226b9-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="226b9-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="226b9-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="226b9-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="226b9-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="226b9-130">**ID3DXEffect ::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="226b9-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




