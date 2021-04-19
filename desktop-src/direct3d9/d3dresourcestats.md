---
description: Statistiques des ressources collectées par le \_ RESOURCEMANAGER D3DDEVINFO lors de l’utilisation du mécanisme de requête asynchrone.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: D3DRESOURCESTATS, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542145"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="2d431-103">D3DRESOURCESTATS, structure</span><span class="sxs-lookup"><span data-stu-id="2d431-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="2d431-104">Statistiques des ressources collectées par le [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) lors de l’utilisation du mécanisme de requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2d431-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d431-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d431-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="2d431-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2d431-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d431-107">**bThrashing**</span><span class="sxs-lookup"><span data-stu-id="2d431-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-109">Indique si une surcharge se produit.</span><span class="sxs-lookup"><span data-stu-id="2d431-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-110">**ApproxBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="2d431-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-112">Nombre approximatif d’octets téléchargés par le gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d431-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-113">**NumEvicts**</span><span class="sxs-lookup"><span data-stu-id="2d431-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-115">Nombre d’objets évincés.</span><span class="sxs-lookup"><span data-stu-id="2d431-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-116">**NumVidCreates**</span><span class="sxs-lookup"><span data-stu-id="2d431-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-118">Nombre d’objets créés dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d431-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-119">**LastPri**</span><span class="sxs-lookup"><span data-stu-id="2d431-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-121">Priorité du dernier objet expulsé.</span><span class="sxs-lookup"><span data-stu-id="2d431-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-122">**NumUsed**</span><span class="sxs-lookup"><span data-stu-id="2d431-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-124">Nombre d’objets définis sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d431-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-125">**NumUsedInVidMem**</span><span class="sxs-lookup"><span data-stu-id="2d431-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-127">Nombre d’objets définis sur l’appareil, qui se trouvent déjà dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d431-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="2d431-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-129">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-130">Nombre d’objets dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d431-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-131">**WorkingSetBytes**</span><span class="sxs-lookup"><span data-stu-id="2d431-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-133">Nombre d’octets dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d431-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-134">**TotalManaged**</span><span class="sxs-lookup"><span data-stu-id="2d431-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-135">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-136">Nombre total d’objets gérés.</span><span class="sxs-lookup"><span data-stu-id="2d431-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="2d431-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="2d431-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="2d431-138">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d431-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2d431-139">Nombre total d’octets d’objets managés.</span><span class="sxs-lookup"><span data-stu-id="2d431-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d431-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d431-140">Requirements</span></span>



| <span data-ttu-id="2d431-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d431-141">Requirement</span></span> | <span data-ttu-id="2d431-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d431-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d431-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d431-143">Header</span></span><br/> | <dl> <span data-ttu-id="2d431-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d431-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d431-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d431-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d431-146">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d431-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2d431-147">Notification asynchrone (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d431-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
