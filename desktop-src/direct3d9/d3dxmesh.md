---
description: 'Énumération D3DXMESH : indicateurs utilisés pour spécifier les options de création d’une maille.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Énumération D3DXMESH (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098097"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="e9b82-103">Énumération D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="e9b82-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="e9b82-104">Indicateurs utilisés pour spécifier les options de création d’une maille.</span><span class="sxs-lookup"><span data-stu-id="e9b82-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9b82-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="e9b82-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e9b82-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e9b82-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**\_32 bits D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e9b82-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-108">Le maillage a des index 32 bits plutôt que des index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e9b82-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="e9b82-109">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e9b82-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="e9b82-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-111">Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**POINTS de D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="e9b82-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-113">Utilisez l’indicateur d’utilisation de [**\_ points D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="e9b82-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-115">Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="e9b82-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-117">Si cet indicateur est spécifié, la mémoire tampon de vertex et d’index du maillage est créée avec l’indicateur [**D3DUSAGE \_ NPATCHES**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="e9b82-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="e9b82-118">Cela est obligatoire si l’objet Mesh doit être rendu à l’aide de l’amélioration N-patch à l’aide de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e9b82-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="e9b82-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-120">Utilisez l’indicateur d’utilisation [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ managé**</span><span class="sxs-lookup"><span data-stu-id="e9b82-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-122">Utilisez l’indicateur d’utilisation [**\_ managée D3DPOOL**](./d3dpool.md) pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="e9b82-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-124">Utilisez l’indicateur d’utilisation [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dynamique**</span><span class="sxs-lookup"><span data-stu-id="e9b82-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-126">Utilisez l’indicateur d’utilisation [**\_ dynamique D3DUSAGE**](d3dusage.md) pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="e9b82-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-128">Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="e9b82-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-130">Utilisez l’indicateur d’utilisation [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ géré**</span><span class="sxs-lookup"><span data-stu-id="e9b82-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-132">Utilisez l’indicateur d’utilisation [**\_ managé D3DPOOL**](./d3dpool.md) pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="e9b82-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-134">Utilisez l’indicateur d’utilisation [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ dynamique**</span><span class="sxs-lookup"><span data-stu-id="e9b82-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-136">Utilisez l’indicateur d’utilisation [**\_ dynamique D3DUSAGE**](d3dusage.md) pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="e9b82-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-138">Utilisez l’indicateur d’utilisation [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="e9b82-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Partage VB \_ D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e9b82-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-140">Force les maillages clonés à partager des mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="e9b82-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-142">Utilisez uniquement le traitement matériel.</span><span class="sxs-lookup"><span data-stu-id="e9b82-142">Use hardware processing only.</span></span> <span data-ttu-id="e9b82-143">Pour les appareils en mode mixte, cet indicateur oblige le système à utiliser le matériel (s’il est pris en charge dans le matériel) ou à traiter par défaut le logiciel.</span><span class="sxs-lookup"><span data-stu-id="e9b82-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="e9b82-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-145">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SYSTEMMEM et D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="e9b82-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**Géré par D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="e9b82-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-147">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Managed et D3DXMESH \_ IB \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="e9b82-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="e9b82-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-149">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ WRITEONLY et D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="e9b82-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamique**</span><span class="sxs-lookup"><span data-stu-id="e9b82-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-151">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Dynamic et D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="e9b82-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="e9b82-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="e9b82-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e9b82-153">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SOFTWAREPROCESSING et D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="e9b82-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9b82-154">Notes </span><span class="sxs-lookup"><span data-stu-id="e9b82-154">Remarks</span></span>

<span data-ttu-id="e9b82-155">Une maille 32 bits (D3DXMESH \_ 32 bits) peut théoriquement prendre en charge (2 ^ 32)-1 face et vertex.</span><span class="sxs-lookup"><span data-stu-id="e9b82-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="e9b82-156">Toutefois, l’allocation de mémoire pour une maille qui est importante sur un système d’exploitation 32 bits n’est pas pratique.</span><span class="sxs-lookup"><span data-stu-id="e9b82-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b82-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9b82-157">Requirements</span></span>



| <span data-ttu-id="e9b82-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9b82-158">Requirement</span></span> | <span data-ttu-id="e9b82-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9b82-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b82-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9b82-160">Header</span></span><br/> | <dl> <span data-ttu-id="e9b82-161"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b82-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b82-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9b82-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b82-163">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="e9b82-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
