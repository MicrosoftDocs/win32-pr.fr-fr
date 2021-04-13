---
description: L’interface ID3DXEffectCompiler compile un effet à partir d’une fonction ou d’un nuanceur de sommets.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interface ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322714"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="1b5a6-103">Interface ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="1b5a6-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="1b5a6-104">L’interface **ID3DXEffectCompiler** compile un effet à partir d’une fonction ou d’un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="1b5a6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1b5a6-105">Members</span></span>

<span data-ttu-id="1b5a6-106">L’interface **ID3DXEffectCompiler** hérite de [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="1b5a6-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="1b5a6-107">**ID3DXEffectCompiler** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1b5a6-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="1b5a6-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b5a6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1b5a6-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b5a6-109">Methods</span></span>

<span data-ttu-id="1b5a6-110">L’interface **ID3DXEffectCompiler** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="1b5a6-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="1b5a6-111">Method</span></span>                                                      | <span data-ttu-id="1b5a6-112">Description</span><span class="sxs-lookup"><span data-stu-id="1b5a6-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b5a6-113">**CompileEffect**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="1b5a6-114">Compilez un effet.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="1b5a6-115">**CompileShader**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="1b5a6-116">Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="1b5a6-117">**GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="1b5a6-118">Obtient un État littéral d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="1b5a6-119">Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="1b5a6-120">**SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="1b5a6-121">Active/désactive l’État littéral d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="1b5a6-122">Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b5a6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1b5a6-123">Remarks</span></span>

<span data-ttu-id="1b5a6-124">L’interface ID3DXEffectCompiler est obtenue en appelant [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)ou [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="1b5a6-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="1b5a6-125">Le type LPD3DXEFFECTCOMPILER est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="1b5a6-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="1b5a6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b5a6-126">Requirements</span></span>



| <span data-ttu-id="1b5a6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b5a6-127">Requirement</span></span> | <span data-ttu-id="1b5a6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b5a6-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5a6-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b5a6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1b5a6-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5a6-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1b5a6-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b5a6-131">Library</span></span><br/> | <dl> <span data-ttu-id="1b5a6-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b5a6-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1b5a6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b5a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b5a6-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1b5a6-135">Interfaces d’effet</span><span class="sxs-lookup"><span data-stu-id="1b5a6-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1b5a6-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="1b5a6-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="1b5a6-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="1b5a6-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




