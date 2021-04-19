---
description: Obtient un paramètre ou une description d’annotation.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect :: GetParameterDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522992"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="8de0a-103">ID3DXBaseEffect :: GetParameterDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="8de0a-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="8de0a-104">Obtient un paramètre ou une description d’annotation.</span><span class="sxs-lookup"><span data-stu-id="8de0a-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8de0a-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8de0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8de0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de0a-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8de0a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8de0a-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8de0a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8de0a-109">Handle de paramètre ou d’annotation.</span><span class="sxs-lookup"><span data-stu-id="8de0a-109">Parameter or annotation handle.</span></span> <span data-ttu-id="8de0a-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8de0a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8de0a-111">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8de0a-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de0a-112">Type : **[ **D3DXPARAMETER \_ desc**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8de0a-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="8de0a-113">Retourne une description du paramètre ou de l’annotation spécifié (e).</span><span class="sxs-lookup"><span data-stu-id="8de0a-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="8de0a-114">Consultez [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="8de0a-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de0a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8de0a-115">Return value</span></span>

<span data-ttu-id="8de0a-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8de0a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8de0a-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8de0a-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8de0a-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8de0a-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8de0a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8de0a-119">Requirements</span></span>



| <span data-ttu-id="8de0a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8de0a-120">Requirement</span></span> | <span data-ttu-id="8de0a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8de0a-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de0a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8de0a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8de0a-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8de0a-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8de0a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8de0a-124">Library</span></span><br/> | <dl> <span data-ttu-id="8de0a-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8de0a-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8de0a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de0a-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8de0a-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




