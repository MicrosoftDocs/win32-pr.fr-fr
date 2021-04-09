---
description: Démarrer la capture des modifications d’État dans un bloc de paramètres.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'ID3DXEffect :: BeginParameterBlock, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043114"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="d668e-103">ID3DXEffect :: BeginParameterBlock, méthode</span><span class="sxs-lookup"><span data-stu-id="d668e-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="d668e-104">Démarrer la capture des modifications d’État dans un bloc de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d668e-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="d668e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d668e-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="d668e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d668e-106">Parameters</span></span>

<span data-ttu-id="d668e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d668e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d668e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d668e-108">Return value</span></span>

<span data-ttu-id="d668e-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d668e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d668e-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d668e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d668e-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="d668e-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d668e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d668e-112">Remarks</span></span>

<span data-ttu-id="d668e-113">L’état du paramètre d’effet de capture change jusqu’à ce que EndParameterBlock soit appelé.</span><span class="sxs-lookup"><span data-stu-id="d668e-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="d668e-114">Les paramètres Effects incluent toutes les modifications d’État en dehors d’une passe.</span><span class="sxs-lookup"><span data-stu-id="d668e-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="d668e-115">Supprimez les blocs de paramètres s’ils ne sont plus nécessaires en appelant DeleteParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="d668e-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="d668e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d668e-116">Requirements</span></span>



| <span data-ttu-id="d668e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d668e-117">Requirement</span></span> | <span data-ttu-id="d668e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d668e-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d668e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d668e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d668e-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d668e-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d668e-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d668e-121">Library</span></span><br/> | <dl> <span data-ttu-id="d668e-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d668e-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d668e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d668e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d668e-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="d668e-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="d668e-125">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d668e-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="d668e-126">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d668e-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="d668e-127">**ID3DXEffect ::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="d668e-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




