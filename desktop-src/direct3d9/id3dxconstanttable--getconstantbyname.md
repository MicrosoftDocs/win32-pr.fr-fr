---
description: 'ID3DXConstantTable :: GetConstantByName, méthode-obtient une constante en recherchant son nom.'
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'ID3DXConstantTable :: GetConstantByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88461a45bf484a72c085f1776eb923a8534b8be3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115247"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="8b641-103">ID3DXConstantTable :: GetConstantByName, méthode</span><span class="sxs-lookup"><span data-stu-id="8b641-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="8b641-104">Obtient une constante en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="8b641-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b641-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b641-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="8b641-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b641-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b641-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b641-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b641-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8b641-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8b641-109">Identificateur unique de la structure de données parent.</span><span class="sxs-lookup"><span data-stu-id="8b641-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="8b641-110">Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8b641-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8b641-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b641-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b641-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b641-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b641-113">Nom de la constante.</span><span class="sxs-lookup"><span data-stu-id="8b641-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b641-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b641-114">Return value</span></span>

<span data-ttu-id="8b641-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8b641-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8b641-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="8b641-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b641-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b641-117">Requirements</span></span>



| <span data-ttu-id="8b641-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b641-118">Requirement</span></span> | <span data-ttu-id="8b641-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b641-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b641-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b641-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8b641-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b641-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8b641-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b641-122">Library</span></span><br/> | <dl> <span data-ttu-id="8b641-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b641-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8b641-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b641-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b641-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8b641-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
