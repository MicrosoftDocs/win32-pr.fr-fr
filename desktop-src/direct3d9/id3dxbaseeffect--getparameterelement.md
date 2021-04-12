---
description: Obtient le handle d’un paramètre d’élément de tableau.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect :: GetParameterElement, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323326"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="5fab9-103">ID3DXBaseEffect :: GetParameterElement, méthode</span><span class="sxs-lookup"><span data-stu-id="5fab9-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="5fab9-104">Obtient le handle d’un paramètre d’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="5fab9-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fab9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fab9-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="5fab9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fab9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fab9-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fab9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fab9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5fab9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5fab9-109">Handle du tableau.</span><span class="sxs-lookup"><span data-stu-id="5fab9-109">Handle of the array.</span></span> <span data-ttu-id="5fab9-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5fab9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fab9-111">*ElementIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fab9-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fab9-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fab9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fab9-113">Index de l’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="5fab9-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fab9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fab9-114">Return value</span></span>

<span data-ttu-id="5fab9-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5fab9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5fab9-116">Retourne le handle du paramètre spécifié, ou **null** si HParameter ou ElementIndex n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5fab9-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="5fab9-117">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5fab9-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fab9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5fab9-118">Remarks</span></span>

<span data-ttu-id="5fab9-119">Cette méthode est utilisée pour obtenir un élément d’un paramètre qui est un tableau.</span><span class="sxs-lookup"><span data-stu-id="5fab9-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fab9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fab9-120">Requirements</span></span>



| <span data-ttu-id="5fab9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fab9-121">Requirement</span></span> | <span data-ttu-id="5fab9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fab9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fab9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fab9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5fab9-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fab9-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5fab9-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5fab9-125">Library</span></span><br/> | <dl> <span data-ttu-id="5fab9-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fab9-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5fab9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fab9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fab9-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5fab9-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
