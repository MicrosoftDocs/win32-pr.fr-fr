---
description: Statistiques d’utilisation des ressources.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Structure D3DDEVINFO_RESOURCEMANAGER (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129978"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="05aee-103">D3DDEVINFO \_ RESOURCEMANAGER, structure</span><span class="sxs-lookup"><span data-stu-id="05aee-103">D3DDEVINFO\_RESOURCEMANAGER structure</span></span>

<span data-ttu-id="05aee-104">Statistiques d’utilisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="05aee-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="05aee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05aee-105">Syntax</span></span>


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a><span data-ttu-id="05aee-106">Membres</span><span class="sxs-lookup"><span data-stu-id="05aee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05aee-107">**stats**</span><span class="sxs-lookup"><span data-stu-id="05aee-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="05aee-108">Type : **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="05aee-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="05aee-109">Tableau d’éléments de statistiques sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="05aee-109">Array of resource statistics elements.</span></span> <span data-ttu-id="05aee-110">Consultez [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="05aee-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05aee-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="05aee-111">Remarks</span></span>

<span data-ttu-id="05aee-112">D3DRTYPECOUNT fait référence au nombre d’énumérations dans [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="05aee-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05aee-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="05aee-113">Requirements</span></span>



| <span data-ttu-id="05aee-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05aee-114">Requirement</span></span> | <span data-ttu-id="05aee-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="05aee-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05aee-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="05aee-116">Header</span></span><br/> | <dl> <span data-ttu-id="05aee-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="05aee-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05aee-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05aee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05aee-119">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="05aee-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
