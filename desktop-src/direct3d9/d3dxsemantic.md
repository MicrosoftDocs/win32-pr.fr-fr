---
description: La sémantique mappe un paramètre aux registres de nuanceur de vertex ou de pixels. Il peut également s’agir de chaînes descriptives facultatives jointes à des paramètres non enregistrés.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: D3DXSEMANTIC, structure (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394104"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="342b9-104">D3DXSEMANTIC, structure</span><span class="sxs-lookup"><span data-stu-id="342b9-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="342b9-105">La sémantique mappe un paramètre aux registres de nuanceur de vertex ou de pixels.</span><span class="sxs-lookup"><span data-stu-id="342b9-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="342b9-106">Il peut également s’agir de chaînes descriptives facultatives jointes à des paramètres non enregistrés.</span><span class="sxs-lookup"><span data-stu-id="342b9-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="342b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="342b9-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="342b9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="342b9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="342b9-109">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="342b9-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="342b9-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="342b9-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="342b9-111">Options qui identifient la façon dont les ressources sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="342b9-111">Options that identify how resources are used.</span></span> <span data-ttu-id="342b9-112">Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="342b9-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="342b9-113">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="342b9-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="342b9-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="342b9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="342b9-115">Options qui modifient la façon dont l’utilisation est interprétée.</span><span class="sxs-lookup"><span data-stu-id="342b9-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="342b9-116">L’index utilisation et utilisation constituent une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="342b9-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="342b9-117">Voir la [déclaration de vertex (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="342b9-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="342b9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="342b9-118">Remarks</span></span>

<span data-ttu-id="342b9-119">La sémantique est requise pour les registres d’entrée et de sortie de nuanceur de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="342b9-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="342b9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="342b9-120">Requirements</span></span>



| <span data-ttu-id="342b9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="342b9-121">Requirement</span></span> | <span data-ttu-id="342b9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="342b9-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="342b9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="342b9-123">Header</span></span><br/> | <dl> <span data-ttu-id="342b9-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="342b9-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="342b9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="342b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342b9-126">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="342b9-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
