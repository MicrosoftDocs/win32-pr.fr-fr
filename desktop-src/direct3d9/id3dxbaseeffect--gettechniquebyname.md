---
description: Obtient le handle d’une technique en recherchant son nom.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect :: GetTechniqueByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522391"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="a2b1f-103">ID3DXBaseEffect :: GetTechniqueByName, méthode</span><span class="sxs-lookup"><span data-stu-id="a2b1f-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="a2b1f-104">Obtient le handle d’une technique en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="a2b1f-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b1f-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="a2b1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2b1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b1f-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2b1f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b1f-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2b1f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2b1f-109">Chaîne contenant le nom de la technique.</span><span class="sxs-lookup"><span data-stu-id="a2b1f-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b1f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2b1f-110">Return value</span></span>

<span data-ttu-id="a2b1f-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a2b1f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a2b1f-112">Retourne le handle de la première technique qui porte le nom spécifié, ou **null** si le nom est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a2b1f-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="a2b1f-113">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a2b1f-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b1f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b1f-114">Requirements</span></span>



| <span data-ttu-id="a2b1f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2b1f-115">Requirement</span></span> | <span data-ttu-id="a2b1f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b1f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b1f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2b1f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2b1f-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b1f-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a2b1f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2b1f-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2b1f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2b1f-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a2b1f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b1f-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a2b1f-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
