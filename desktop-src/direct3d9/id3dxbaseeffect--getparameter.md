---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect :: GetParameter, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043184"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="76900-103">ID3DXBaseEffect :: GetParameter, méthode</span><span class="sxs-lookup"><span data-stu-id="76900-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="76900-104">Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure.</span><span class="sxs-lookup"><span data-stu-id="76900-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="76900-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76900-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="76900-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76900-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76900-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76900-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="76900-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="76900-109">Handle du paramètre, ou **null** pour les paramètres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="76900-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="76900-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="76900-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="76900-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76900-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76900-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76900-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76900-113">Index du paramètre.</span><span class="sxs-lookup"><span data-stu-id="76900-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76900-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76900-114">Return value</span></span>

<span data-ttu-id="76900-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="76900-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="76900-116">Retourne le handle du paramètre spécifié, ou **null** si l’index n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="76900-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="76900-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="76900-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76900-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76900-118">Requirements</span></span>



| <span data-ttu-id="76900-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76900-119">Requirement</span></span> | <span data-ttu-id="76900-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="76900-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76900-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="76900-121">Header</span></span><br/>  | <dl> <span data-ttu-id="76900-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="76900-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="76900-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76900-123">Library</span></span><br/> | <dl> <span data-ttu-id="76900-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76900-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="76900-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76900-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76900-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="76900-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
