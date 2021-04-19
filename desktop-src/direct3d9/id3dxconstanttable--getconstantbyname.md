---
description: Obtient une constante en recherchant son nom.
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
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538744"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="357f9-103">ID3DXConstantTable :: GetConstantByName, méthode</span><span class="sxs-lookup"><span data-stu-id="357f9-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="357f9-104">Obtient une constante en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="357f9-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="357f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="357f9-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="357f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="357f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="357f9-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="357f9-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357f9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="357f9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="357f9-109">Identificateur unique de la structure de données parent.</span><span class="sxs-lookup"><span data-stu-id="357f9-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="357f9-110">Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="357f9-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="357f9-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="357f9-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="357f9-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="357f9-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="357f9-113">Nom de la constante.</span><span class="sxs-lookup"><span data-stu-id="357f9-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="357f9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="357f9-114">Return value</span></span>

<span data-ttu-id="357f9-115">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="357f9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="357f9-116">Retourne un identificateur unique à la constante.</span><span class="sxs-lookup"><span data-stu-id="357f9-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="357f9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="357f9-117">Requirements</span></span>



| <span data-ttu-id="357f9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="357f9-118">Requirement</span></span> | <span data-ttu-id="357f9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="357f9-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="357f9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="357f9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="357f9-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="357f9-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="357f9-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="357f9-122">Library</span></span><br/> | <dl> <span data-ttu-id="357f9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="357f9-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="357f9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="357f9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357f9-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="357f9-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
