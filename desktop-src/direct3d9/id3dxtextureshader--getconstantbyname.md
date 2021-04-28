---
description: 'ID3DXTextureShader :: GetConstantByName, méthode-obtient une constante en recherchant son nom.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'ID3DXTextureShader :: GetConstantByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117657"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="7ad39-103">ID3DXTextureShader :: GetConstantByName, méthode</span><span class="sxs-lookup"><span data-stu-id="7ad39-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="7ad39-104">Obtient une constante en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="7ad39-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ad39-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="7ad39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ad39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad39-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad39-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad39-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7ad39-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7ad39-109">[Handle](handles.md) de la structure de données parent.</span><span class="sxs-lookup"><span data-stu-id="7ad39-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="7ad39-110">Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7ad39-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ad39-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ad39-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ad39-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ad39-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ad39-113">Chaîne contenant le nom de la constante.</span><span class="sxs-lookup"><span data-stu-id="7ad39-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad39-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ad39-114">Return value</span></span>

<span data-ttu-id="7ad39-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7ad39-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7ad39-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="7ad39-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad39-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ad39-117">Requirements</span></span>



| <span data-ttu-id="7ad39-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ad39-118">Requirement</span></span> | <span data-ttu-id="7ad39-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ad39-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad39-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ad39-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ad39-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad39-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7ad39-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ad39-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ad39-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad39-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7ad39-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ad39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad39-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="7ad39-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
