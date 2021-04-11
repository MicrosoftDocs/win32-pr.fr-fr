---
description: Détermine si un paramètre est utilisé par la technique.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'ID3DXEffect :: IsParameterUsed, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116186"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="88bf9-103">ID3DXEffect :: IsParameterUsed, méthode</span><span class="sxs-lookup"><span data-stu-id="88bf9-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="88bf9-104">Détermine si un paramètre est utilisé par la technique.</span><span class="sxs-lookup"><span data-stu-id="88bf9-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="88bf9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88bf9-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="88bf9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88bf9-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88bf9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88bf9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88bf9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88bf9-109">Identificateur unique du paramètre.</span><span class="sxs-lookup"><span data-stu-id="88bf9-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="88bf9-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="88bf9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="88bf9-111">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88bf9-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88bf9-112">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88bf9-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88bf9-113">Identificateur unique de la technique.</span><span class="sxs-lookup"><span data-stu-id="88bf9-113">Unique identifier for the technique.</span></span> <span data-ttu-id="88bf9-114">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="88bf9-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88bf9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88bf9-115">Return value</span></span>

<span data-ttu-id="88bf9-116">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88bf9-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88bf9-117">Retourne la **valeur true** si le paramètre est utilisé et retourne la **valeur false** si le paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="88bf9-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="88bf9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88bf9-118">Requirements</span></span>



| <span data-ttu-id="88bf9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88bf9-119">Requirement</span></span> | <span data-ttu-id="88bf9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="88bf9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88bf9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="88bf9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="88bf9-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="88bf9-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="88bf9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88bf9-123">Library</span></span><br/> | <dl> <span data-ttu-id="88bf9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88bf9-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="88bf9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88bf9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88bf9-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="88bf9-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
