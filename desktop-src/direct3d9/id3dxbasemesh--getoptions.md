---
description: Récupère les options de maillage activées pour ce maillage au moment de la création.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh :: GetOptions, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527122"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="dd6df-103">ID3DXBaseMesh :: GetOptions, méthode</span><span class="sxs-lookup"><span data-stu-id="dd6df-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="dd6df-104">Récupère les options de maillage activées pour ce maillage au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="dd6df-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd6df-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="dd6df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd6df-106">Parameters</span></span>

<span data-ttu-id="dd6df-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd6df-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd6df-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd6df-108">Return value</span></span>

<span data-ttu-id="dd6df-109">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6df-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd6df-110">Retourne une combinaison d’un ou plusieurs des indicateurs suivants, indiquant les options activées pour ce maillage au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="dd6df-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="dd6df-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd6df-111">Value</span></span>                   | <span data-ttu-id="dd6df-112">Description</span><span class="sxs-lookup"><span data-stu-id="dd6df-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6df-113">\_32 bits D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="dd6df-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="dd6df-114">Utilisez des index 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd6df-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="dd6df-115">D3DXMESH \_ DONOTCLIP</span><span class="sxs-lookup"><span data-stu-id="dd6df-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="dd6df-116">Utilisez l' \_ indicateur d’utilisation D3DUSAGE DONOTCLIP pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="dd6df-117">D3DXMESH \_ dynamique</span><span class="sxs-lookup"><span data-stu-id="dd6df-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="dd6df-118">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Dynamic et D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="dd6df-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="dd6df-119">D3DXMESH \_ RTPATCHES</span><span class="sxs-lookup"><span data-stu-id="dd6df-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="dd6df-120">Utilisez l' \_ indicateur d’utilisation D3DUSAGE RTPATCHES pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="dd6df-121">D3DXMESH \_ NPATCHES</span><span class="sxs-lookup"><span data-stu-id="dd6df-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="dd6df-122">Si cet indicateur est spécifié, la mémoire tampon de vertex et d’index du maillage est créée avec l' \_ indicateur D3DUSAGE NPATCHES.</span><span class="sxs-lookup"><span data-stu-id="dd6df-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="dd6df-123">Cela est obligatoire si l’objet Mesh doit être rendu à l’aide de l’amélioration N-patch.</span><span class="sxs-lookup"><span data-stu-id="dd6df-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="dd6df-124">Géré par D3DXMESH \_</span><span class="sxs-lookup"><span data-stu-id="dd6df-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="dd6df-125">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Managed et D3DXMESH \_ IB \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="dd6df-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="dd6df-126">POINTS de D3DXMESH \_</span><span class="sxs-lookup"><span data-stu-id="dd6df-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="dd6df-127">Utilisez l' \_ indicateur d’utilisation de points D3DUSAGE pour les mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="dd6df-128">D3DXMESH \_ IB \_ dynamique</span><span class="sxs-lookup"><span data-stu-id="dd6df-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="dd6df-129">Utilisez l' \_ indicateur d’utilisation dynamique D3DUSAGE pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="dd6df-130">D3DXMESH \_ IB \_ géré</span><span class="sxs-lookup"><span data-stu-id="dd6df-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="dd6df-131">Utilisez la \_ classe de mémoire managée D3DPOOL pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="dd6df-132">D3DXMESH \_ IB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="dd6df-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="dd6df-133">Utilisez la \_ classe de mémoire D3DPOOL SYSTEMMEM pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="dd6df-134">D3DXMESH \_ IB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="dd6df-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="dd6df-135">Utilisez l' \_ indicateur d’utilisation WRITEONLY D3DUSAGE pour les mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="dd6df-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="dd6df-136">D3DXMESH \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="dd6df-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="dd6df-137">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SYSTEMMEM et D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="dd6df-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="dd6df-138">D3DXMESH \_ VB \_ dynamique</span><span class="sxs-lookup"><span data-stu-id="dd6df-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="dd6df-139">Utilisez l' \_ indicateur d’utilisation dynamique D3DUSAGE pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="dd6df-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="dd6df-140">D3DXMESH \_ VB \_ managé</span><span class="sxs-lookup"><span data-stu-id="dd6df-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="dd6df-141">Utilisez la \_ classe de mémoire managée D3DPOOL pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="dd6df-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="dd6df-142">D3DXMESH \_ VB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="dd6df-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="dd6df-143">Utilisez la \_ classe de mémoire D3DPOOL SYSTEMMEM pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="dd6df-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="dd6df-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="dd6df-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="dd6df-145">Utilisez l' \_ indicateur d’utilisation WRITEONLY D3DUSAGE pour les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="dd6df-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="dd6df-146">D3DXMESH \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="dd6df-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="dd6df-147">Équivaut à spécifier à la fois D3DXMESH \_ VB \_ WRITEONLY et D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="dd6df-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="dd6df-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd6df-148">Requirements</span></span>



| <span data-ttu-id="dd6df-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd6df-149">Requirement</span></span> | <span data-ttu-id="dd6df-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd6df-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6df-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd6df-151">Header</span></span><br/>  | <dl> <span data-ttu-id="dd6df-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd6df-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dd6df-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd6df-153">Library</span></span><br/> | <dl> <span data-ttu-id="dd6df-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd6df-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd6df-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd6df-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6df-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="dd6df-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
