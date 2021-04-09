---
description: Arrêter la capture des modifications d’état des paramètres d’effet.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'ID3DXEffect :: EndParameterBlock, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953870"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="f5082-103">ID3DXEffect :: EndParameterBlock, méthode</span><span class="sxs-lookup"><span data-stu-id="f5082-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="f5082-104">Arrêter la capture des modifications d’état des paramètres d’effet.</span><span class="sxs-lookup"><span data-stu-id="f5082-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5082-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5082-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="f5082-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5082-106">Parameters</span></span>

<span data-ttu-id="f5082-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f5082-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5082-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5082-108">Return value</span></span>

<span data-ttu-id="f5082-109">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f5082-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f5082-110">Retourne un handle vers le bloc d’État du paramètre.</span><span class="sxs-lookup"><span data-stu-id="f5082-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5082-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f5082-111">Remarks</span></span>

<span data-ttu-id="f5082-112">Tous les paramètres d’effet qui changent d’État (après l’appel de BeginParameterBlock et avant l’appel de EndParameterBlock) sont enregistrés dans un bloc d’état de paramètre d’effet.</span><span class="sxs-lookup"><span data-stu-id="f5082-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="f5082-113">Utilisez ApplyParameterBlock pour appliquer ce bloc de modifications d’État au système d’effet.</span><span class="sxs-lookup"><span data-stu-id="f5082-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="f5082-114">Une fois que vous avez fini d’utiliser un bloc d’État, utilisez DeleteParameterBlock pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f5082-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5082-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5082-115">Requirements</span></span>



| <span data-ttu-id="f5082-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5082-116">Requirement</span></span> | <span data-ttu-id="f5082-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5082-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5082-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5082-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f5082-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5082-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f5082-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5082-120">Library</span></span><br/> | <dl> <span data-ttu-id="f5082-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5082-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f5082-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5082-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5082-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f5082-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="f5082-124">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f5082-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="f5082-125">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f5082-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="f5082-126">**ID3DXEffect ::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="f5082-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




