---
description: Description de la table constante.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: Structure D3DXCONSTANTTABLE_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762097"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="92c1d-103">D3DXCONSTANTTABLE \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="92c1d-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="92c1d-104">Description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="92c1d-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92c1d-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="92c1d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="92c1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="92c1d-107">**Creator**</span><span class="sxs-lookup"><span data-stu-id="92c1d-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="92c1d-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c1d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92c1d-109">Nom du créateur de la table constante.</span><span class="sxs-lookup"><span data-stu-id="92c1d-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="92c1d-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="92c1d-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="92c1d-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c1d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92c1d-112">Version du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="92c1d-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="92c1d-113">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="92c1d-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="92c1d-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c1d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92c1d-115">Nombre de constantes dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="92c1d-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92c1d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92c1d-116">Requirements</span></span>



| <span data-ttu-id="92c1d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92c1d-117">Requirement</span></span> | <span data-ttu-id="92c1d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="92c1d-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c1d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="92c1d-119">Header</span></span><br/> | <dl> <span data-ttu-id="92c1d-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c1d-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c1d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92c1d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c1d-122">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="92c1d-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="92c1d-123">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="92c1d-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
