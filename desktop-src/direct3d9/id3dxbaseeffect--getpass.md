---
description: Obtient le handle d’une passe.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect :: GetPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394251"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="2bc60-103">ID3DXBaseEffect :: GetPass, méthode</span><span class="sxs-lookup"><span data-stu-id="2bc60-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="2bc60-104">Obtient le handle d’une passe.</span><span class="sxs-lookup"><span data-stu-id="2bc60-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bc60-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="2bc60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bc60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc60-107">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bc60-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc60-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2bc60-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2bc60-109">Handle de la technique parente.</span><span class="sxs-lookup"><span data-stu-id="2bc60-109">Handle of the parent technique.</span></span> <span data-ttu-id="2bc60-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2bc60-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bc60-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bc60-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc60-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bc60-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bc60-113">Index pour la passe.</span><span class="sxs-lookup"><span data-stu-id="2bc60-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc60-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bc60-114">Return value</span></span>

<span data-ttu-id="2bc60-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2bc60-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2bc60-116">Retourne le handle de la passe spécifiée à l’intérieur de la technique spécifiée, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2bc60-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="2bc60-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2bc60-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc60-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bc60-118">Requirements</span></span>



| <span data-ttu-id="2bc60-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bc60-119">Requirement</span></span> | <span data-ttu-id="2bc60-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bc60-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc60-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bc60-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2bc60-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc60-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2bc60-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2bc60-123">Library</span></span><br/> | <dl> <span data-ttu-id="2bc60-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bc60-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2bc60-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bc60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc60-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2bc60-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
