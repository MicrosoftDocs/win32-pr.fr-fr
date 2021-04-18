---
description: Obtient une constante de la table constante.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader :: GetConstantElement, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211789"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="5d521-103">ID3DXTextureShader :: GetConstantElement, méthode</span><span class="sxs-lookup"><span data-stu-id="5d521-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="5d521-104">Obtient une constante de la table constante.</span><span class="sxs-lookup"><span data-stu-id="5d521-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d521-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d521-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="5d521-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d521-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d521-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d521-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d521-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5d521-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5d521-109">[Handle](handles.md) vers le tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="5d521-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="5d521-110">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="5d521-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5d521-111">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d521-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d521-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d521-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d521-113">Index de base zéro de l’élément dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="5d521-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d521-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d521-114">Return value</span></span>

<span data-ttu-id="5d521-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5d521-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5d521-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="5d521-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d521-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5d521-117">Remarks</span></span>

<span data-ttu-id="5d521-118">Pour obtenir une constante qui ne fait pas partie d’un tableau, utilisez [**ID3DXTextureShader :: GetConstant**](id3dxtextureshader--getconstant.md) ou [**ID3DXTextureShader :: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="5d521-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d521-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d521-119">Requirements</span></span>



| <span data-ttu-id="5d521-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d521-120">Requirement</span></span> | <span data-ttu-id="5d521-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d521-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d521-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d521-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5d521-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d521-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5d521-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d521-124">Library</span></span><br/> | <dl> <span data-ttu-id="5d521-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d521-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5d521-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d521-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d521-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="5d521-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
