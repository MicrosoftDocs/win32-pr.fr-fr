---
description: 'ID3DXTextureShader :: GetConstant, méthode-obtient une constante en recherchant son index.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'ID3DXTextureShader :: GetConstant, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117667"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="9a9a8-103">ID3DXTextureShader :: GetConstant, méthode</span><span class="sxs-lookup"><span data-stu-id="9a9a8-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="9a9a8-104">Obtient une constante en recherchant son index.</span><span class="sxs-lookup"><span data-stu-id="9a9a8-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a9a8-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="9a9a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a9a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9a8-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a9a8-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9a8-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9a9a8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9a9a8-109">[Handle](handles.md) de la structure de données parent.</span><span class="sxs-lookup"><span data-stu-id="9a9a8-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="9a9a8-110">Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9a9a8-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9a9a8-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a9a8-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9a8-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a9a8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a9a8-113">Index de base zéro de la constante.</span><span class="sxs-lookup"><span data-stu-id="9a9a8-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9a8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a9a8-114">Return value</span></span>

<span data-ttu-id="9a9a8-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9a9a8-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9a9a8-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="9a9a8-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a9a8-117">Notes </span><span class="sxs-lookup"><span data-stu-id="9a9a8-117">Remarks</span></span>

<span data-ttu-id="9a9a8-118">Pour obtenir une constante d’un tableau de constantes, utilisez [**ID3DXTextureShader :: GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a9a8-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a9a8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a9a8-119">Requirements</span></span>



| <span data-ttu-id="9a9a8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a9a8-120">Requirement</span></span> | <span data-ttu-id="9a9a8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a9a8-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9a8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a9a8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a9a8-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9a8-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9a9a8-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a9a8-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a9a8-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a9a8-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9a9a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a9a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9a8-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9a9a8-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
