---
description: Obtient une description de technique.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect :: GetTechniqueDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211941"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="b45e5-103">ID3DXBaseEffect :: GetTechniqueDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="b45e5-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="b45e5-104">Obtient une description de technique.</span><span class="sxs-lookup"><span data-stu-id="b45e5-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b45e5-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b45e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b45e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45e5-107">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b45e5-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b45e5-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b45e5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b45e5-109">Handle de technique.</span><span class="sxs-lookup"><span data-stu-id="b45e5-109">Technique handle.</span></span> <span data-ttu-id="b45e5-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b45e5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b45e5-111">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b45e5-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b45e5-112">Type : **[ **D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b45e5-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="b45e5-113">Retourne une description de la technique.</span><span class="sxs-lookup"><span data-stu-id="b45e5-113">Returns a description of the technique.</span></span> <span data-ttu-id="b45e5-114">Consultez [**D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b45e5-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45e5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b45e5-115">Return value</span></span>

<span data-ttu-id="b45e5-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b45e5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b45e5-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b45e5-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b45e5-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b45e5-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45e5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b45e5-119">Requirements</span></span>



| <span data-ttu-id="b45e5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b45e5-120">Requirement</span></span> | <span data-ttu-id="b45e5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b45e5-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45e5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b45e5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b45e5-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45e5-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b45e5-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b45e5-124">Library</span></span><br/> | <dl> <span data-ttu-id="b45e5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b45e5-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b45e5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b45e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45e5-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b45e5-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




