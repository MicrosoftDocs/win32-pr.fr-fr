---
description: Indicateurs d’optimisation du cache de vertex.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Structure D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529249"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="bb22e-103">D3DDEVINFO \_ Vcache, structure</span><span class="sxs-lookup"><span data-stu-id="bb22e-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="bb22e-104">Indicateurs d’optimisation du cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="bb22e-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb22e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb22e-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="bb22e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="bb22e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb22e-107">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="bb22e-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="bb22e-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb22e-109">Modèle binaire.</span><span class="sxs-lookup"><span data-stu-id="bb22e-109">Bit pattern.</span></span> <span data-ttu-id="bb22e-110">La valeur de retour doit être le FOURCC ('C', 'A', 'C', 'H').</span><span class="sxs-lookup"><span data-stu-id="bb22e-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="bb22e-111">**OptMethod**</span><span class="sxs-lookup"><span data-stu-id="bb22e-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="bb22e-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb22e-113">Méthode Optimizations.</span><span class="sxs-lookup"><span data-stu-id="bb22e-113">Optimizations method.</span></span> <span data-ttu-id="bb22e-114">Utilisez 0 pour récupérer les bandes les plus longues.</span><span class="sxs-lookup"><span data-stu-id="bb22e-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="bb22e-115">Utilisez 1 pour optimiser l’utilisation du cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="bb22e-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="bb22e-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="bb22e-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb22e-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22e-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb22e-118">Taille du cache utilisée comme cible pour l’optimisation.</span><span class="sxs-lookup"><span data-stu-id="bb22e-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="bb22e-119">Cela est requis uniquement si OptMethod est 1.</span><span class="sxs-lookup"><span data-stu-id="bb22e-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="bb22e-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="bb22e-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="bb22e-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb22e-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb22e-122">Utilisé par les méthodes d’optimisation internes pour déterminer le moment du redémarrage des bandes.</span><span class="sxs-lookup"><span data-stu-id="bb22e-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="bb22e-123">Cela ne peut pas être défini ou modifié par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bb22e-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="bb22e-124">Cela est requis uniquement si OptMethod est 1.</span><span class="sxs-lookup"><span data-stu-id="bb22e-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb22e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb22e-125">Requirements</span></span>



| <span data-ttu-id="bb22e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb22e-126">Requirement</span></span> | <span data-ttu-id="bb22e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb22e-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb22e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb22e-128">Header</span></span><br/> | <dl> <span data-ttu-id="bb22e-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb22e-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb22e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb22e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb22e-131">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="bb22e-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="bb22e-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="bb22e-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
