---
description: Statistiques d’utilisation des ressources.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Structure D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761966"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="4f347-103">D3DDEVINFO \_ ResourceManager, structure</span><span class="sxs-lookup"><span data-stu-id="4f347-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="4f347-104">Statistiques d’utilisation des ressources.</span><span class="sxs-lookup"><span data-stu-id="4f347-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f347-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f347-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="4f347-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4f347-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f347-107">**stats**</span><span class="sxs-lookup"><span data-stu-id="4f347-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="4f347-108">Type : **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="4f347-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f347-109">Tableau d’éléments de statistiques sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="4f347-109">Array of resource statistics elements.</span></span> <span data-ttu-id="4f347-110">Consultez [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="4f347-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f347-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4f347-111">Remarks</span></span>

<span data-ttu-id="4f347-112">D3DRTYPECOUNT fait référence au nombre d’énumérations dans [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="4f347-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f347-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f347-113">Requirements</span></span>



| <span data-ttu-id="4f347-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f347-114">Requirement</span></span> | <span data-ttu-id="4f347-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f347-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f347-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f347-116">Header</span></span><br/> | <dl> <span data-ttu-id="4f347-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f347-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f347-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f347-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f347-119">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f347-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
