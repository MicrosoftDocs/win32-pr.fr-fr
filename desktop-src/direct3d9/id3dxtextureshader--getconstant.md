---
description: Obtient une constante en recherchant son index.
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
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537279"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="af11c-103">ID3DXTextureShader :: GetConstant, méthode</span><span class="sxs-lookup"><span data-stu-id="af11c-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="af11c-104">Obtient une constante en recherchant son index.</span><span class="sxs-lookup"><span data-stu-id="af11c-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="af11c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af11c-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="af11c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af11c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af11c-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af11c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af11c-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af11c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af11c-109">[Handle](handles.md) de la structure de données parent.</span><span class="sxs-lookup"><span data-stu-id="af11c-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="af11c-110">Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="af11c-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="af11c-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af11c-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af11c-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af11c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af11c-113">Index de base zéro de la constante.</span><span class="sxs-lookup"><span data-stu-id="af11c-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af11c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af11c-114">Return value</span></span>

<span data-ttu-id="af11c-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af11c-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af11c-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="af11c-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="af11c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="af11c-117">Remarks</span></span>

<span data-ttu-id="af11c-118">Pour obtenir une constante d’un tableau de constantes, utilisez [**ID3DXTextureShader :: GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="af11c-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af11c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af11c-119">Requirements</span></span>



| <span data-ttu-id="af11c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af11c-120">Requirement</span></span> | <span data-ttu-id="af11c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="af11c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af11c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="af11c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="af11c-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="af11c-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="af11c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af11c-124">Library</span></span><br/> | <dl> <span data-ttu-id="af11c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af11c-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="af11c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af11c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af11c-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="af11c-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
