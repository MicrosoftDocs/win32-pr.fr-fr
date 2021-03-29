---
description: Comment le pipeline interprète les données de vertex qui sont liées à l’étape assembleur d’entrée. Ces valeurs de topologie primitives déterminent la façon dont les données de vertex sont restituées à l’écran.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Énumération de la topologie primitive d3d11 \_'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991857"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="1e1f1-104">\_Énumération de la topologie primitive d3d11 \_</span><span class="sxs-lookup"><span data-stu-id="1e1f1-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="1e1f1-105">Comment le pipeline interprète les données de vertex qui sont liées à l’étape assembleur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="1e1f1-106">Ces valeurs de topologie primitives déterminent la façon dont les données de vertex sont restituées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e1f1-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="1e1f1-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e1f1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e1f1-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologie primitive d3d11 \_ \_ non définie**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-110">L’étape IA n’a pas été initialisée avec une topologie primitive.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="1e1f1-111">L’étape IA ne fonctionnera pas correctement, sauf si une topologie primitive est définie.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**\_Topologie primitive d3d11 \_ \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-113">Interpréter les données de vertex comme une liste de points.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Topologie primitive d3d11 \_ \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-115">Interpréter les données de vertex comme une liste de lignes.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_Topologie primitive d3d11 \_ \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-117">Interpréter les données de vertex comme une bande de courbes.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_Topologie primitive d3d11 \_ \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-119">Interpréter les données de vertex comme une liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_Topologie primitive d3d11 \_ \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-121">Interpréter les données de vertex comme une bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ primitive \_ \_ LINELIST \_ adj**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-123">Interpréter les données de vertex comme une liste de lignes avec des données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ primitive \_ \_ LINESTRIP \_ adj**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-125">Interpréter les données de vertex comme une bande de lignes avec des données d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ primitive \_ \_ TRIANGLELIST \_ adj**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-127">Interpréter les données de vertex comme une liste de triangles avec les données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ primitive \_ \_ TRIANGLESTRIP \_ adj**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-129">Interpréter les données de vertex comme une bande triangulaire avec des données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 1 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-131">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 2 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-133">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 3 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-135">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 4 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-137">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 5 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-139">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 6 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-141">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 7 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-143">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 8 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-145">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 9 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-147">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 10 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-149">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 11 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-151">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 12 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-153">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 13 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-155">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 14 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-157">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 15 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-159">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 16 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-161">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 17 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-163">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**\_Topologie primitive d3d11- \_ point de \_ \_ contrôle 18 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-165">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 19 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-167">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 20 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-169">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ primitive primitive \_ \_ 21 point \_ de \_ contrôle \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-171">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 22 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-173">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ primitive de la \_ topologie de point de \_ \_ contrôle 23 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-175">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 24 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-177">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ primitive \_ PATCHLIST, \_ \_ point de contrôle 25 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-179">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**\_Point de contrôle de topologie d3d11 primitive \_ \_ 26 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-181">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 27 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-183">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 28 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-185">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 29 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-187">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 30 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-189">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 31 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-191">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f1-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**\_Topologie primitive D3D11 \_ \_ 32 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="1e1f1-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1e1f1-193">Interpréter les données de vertex comme une liste de correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e1f1-194">Notes</span><span class="sxs-lookup"><span data-stu-id="1e1f1-194">Remarks</span></span>

<span data-ttu-id="1e1f1-195">L’énumération de la **\_ \_ topologie primitive d3d11** est de type défini dans le fichier d’en-tête d3d11. h comme une ÉNUMÉRation de la topologie de la [**\_ primitive \_ D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , qui est entièrement définie dans le fichier d’en-tête D3DCommon. h.</span><span class="sxs-lookup"><span data-stu-id="1e1f1-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
