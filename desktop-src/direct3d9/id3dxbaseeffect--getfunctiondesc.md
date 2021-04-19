---
description: Obtient une description de fonction.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect :: GetFunctionDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545313"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="7520e-103">ID3DXBaseEffect :: GetFunctionDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="7520e-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="7520e-104">Obtient une description de fonction.</span><span class="sxs-lookup"><span data-stu-id="7520e-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7520e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7520e-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7520e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7520e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7520e-107">*hFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7520e-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7520e-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7520e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7520e-109">Handle de fonction.</span><span class="sxs-lookup"><span data-stu-id="7520e-109">Function handle.</span></span> <span data-ttu-id="7520e-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7520e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7520e-111">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7520e-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7520e-112">Type : **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7520e-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="7520e-113">Retourne une description de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7520e-113">Returns a description of the function.</span></span> <span data-ttu-id="7520e-114">Consultez [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="7520e-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7520e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7520e-115">Return value</span></span>

<span data-ttu-id="7520e-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7520e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7520e-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7520e-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7520e-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7520e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7520e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7520e-119">Requirements</span></span>



| <span data-ttu-id="7520e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7520e-120">Requirement</span></span> | <span data-ttu-id="7520e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7520e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7520e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7520e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7520e-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7520e-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7520e-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7520e-124">Library</span></span><br/> | <dl> <span data-ttu-id="7520e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7520e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7520e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7520e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7520e-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7520e-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




