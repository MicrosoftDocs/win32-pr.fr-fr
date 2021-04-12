---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant sa sémantique à l’aide d’une recherche qui ne respecte pas la casse.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect :: GetParameterBySemantic, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323329"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="675c9-103">ID3DXBaseEffect :: GetParameterBySemantic, méthode</span><span class="sxs-lookup"><span data-stu-id="675c9-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="675c9-104">Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant sa sémantique à l’aide d’une recherche qui ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="675c9-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="675c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="675c9-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="675c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="675c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="675c9-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="675c9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="675c9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="675c9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="675c9-109">Handle du paramètre, ou **null** pour les paramètres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="675c9-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="675c9-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="675c9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="675c9-111">*pSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="675c9-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="675c9-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="675c9-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="675c9-113">Chaîne contenant le nom sémantique.</span><span class="sxs-lookup"><span data-stu-id="675c9-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="675c9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="675c9-114">Return value</span></span>

<span data-ttu-id="675c9-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="675c9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="675c9-116">Retourne le handle du premier paramètre qui correspond à la sémantique spécifiée, ou **null** si la sémantique est introuvable.</span><span class="sxs-lookup"><span data-stu-id="675c9-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="675c9-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="675c9-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="675c9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="675c9-118">Requirements</span></span>



| <span data-ttu-id="675c9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="675c9-119">Requirement</span></span> | <span data-ttu-id="675c9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="675c9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="675c9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="675c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="675c9-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="675c9-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="675c9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="675c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="675c9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="675c9-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="675c9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="675c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675c9-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="675c9-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
