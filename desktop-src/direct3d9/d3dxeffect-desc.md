---
description: Décrit un objet Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Structure D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762055"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="8cfa2-103">D3DXEFFECT \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="8cfa2-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="8cfa2-104">Décrit un objet Effect.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfa2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cfa2-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="8cfa2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8cfa2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8cfa2-107">**Creator**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="8cfa2-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8cfa2-109">Chaîne qui contient le nom du créateur de l’effet.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="8cfa2-110">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="8cfa2-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8cfa2-112">Nombre de paramètres utilisés pour l’effet.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="8cfa2-113">**Technologie**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="8cfa2-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8cfa2-115">Nombre de techniques pouvant rendre l’effet.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="8cfa2-116">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="8cfa2-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cfa2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8cfa2-118">Nombre de fonctions qui peuvent rendre l’effet.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cfa2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8cfa2-119">Remarks</span></span>

<span data-ttu-id="8cfa2-120">Un objet Effect peut contenir plusieurs techniques et paramètres de rendu pour le même effet.</span><span class="sxs-lookup"><span data-stu-id="8cfa2-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfa2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cfa2-121">Requirements</span></span>



| <span data-ttu-id="8cfa2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cfa2-122">Requirement</span></span> | <span data-ttu-id="8cfa2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cfa2-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfa2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cfa2-124">Header</span></span><br/> | <dl> <span data-ttu-id="8cfa2-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cfa2-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cfa2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cfa2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfa2-127">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="8cfa2-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
