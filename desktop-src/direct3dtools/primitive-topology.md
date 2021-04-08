---
description: Énumération utilisée pour indiquer la topologie d’un maillage. Consultez MeshDataVertCallback.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PRIMITIVE_TOPOLOGY
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033548"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="c4698-104"><span id="vspixengine.primitive_topology"></span>\_Énumération de la topologie primitive</span><span class="sxs-lookup"><span data-stu-id="c4698-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="c4698-105">Énumération utilisée pour indiquer la topologie d’un maillage.</span><span class="sxs-lookup"><span data-stu-id="c4698-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="c4698-106">Consultez MeshDataVertCallback.</span><span class="sxs-lookup"><span data-stu-id="c4698-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4698-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4698-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="c4698-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c4698-108">Constants</span></span>

<span data-ttu-id="c4698-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**\_topologie primitive \_ non définie**</span><span class="sxs-lookup"><span data-stu-id="c4698-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="c4698-110">La topologie du maillage n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c4698-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="c4698-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**\_topologie primitive \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="c4698-112">La topologie du maillage est une liste de points.</span><span class="sxs-lookup"><span data-stu-id="c4698-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="c4698-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**\_topologie primitive \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="c4698-114">La topologie de la maille est une liste de lignes.</span><span class="sxs-lookup"><span data-stu-id="c4698-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="c4698-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**\_topologie primitive \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="c4698-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="c4698-116">La topologie du maillage est une bande.</span><span class="sxs-lookup"><span data-stu-id="c4698-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="c4698-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**\_topologie primitive \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="c4698-118">La topologie de la maille est une liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="c4698-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="c4698-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**\_topologie primitive \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="c4698-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="c4698-120">La topologie de la maille est une bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="c4698-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="c4698-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**\_topologie primitive \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="c4698-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="c4698-122">La topologie du maillage est un ventilateur triangulaire.</span><span class="sxs-lookup"><span data-stu-id="c4698-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="c4698-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**\_topologie primitive \_ LINELIST \_ adj**</span><span class="sxs-lookup"><span data-stu-id="c4698-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="c4698-124">La topologie de la maille est une liste de lignes avec contiguïté.</span><span class="sxs-lookup"><span data-stu-id="c4698-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="c4698-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**\_topologie primitive \_ LINESTRIP \_ adj**</span><span class="sxs-lookup"><span data-stu-id="c4698-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="c4698-126">La topologie du maillage est une bande avec contiguïté.</span><span class="sxs-lookup"><span data-stu-id="c4698-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="c4698-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**\_topologie primitive \_ TRIANGLELIST \_ adj**</span><span class="sxs-lookup"><span data-stu-id="c4698-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="c4698-128">La topologie de la maille est une liste de triangles avec contiguïté.</span><span class="sxs-lookup"><span data-stu-id="c4698-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="c4698-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**\_topologie primitive \_ TRIANGLESTRIP \_ adj**</span><span class="sxs-lookup"><span data-stu-id="c4698-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="c4698-130">La topologie de la maille est une bande triangulaire avec contiguïté.</span><span class="sxs-lookup"><span data-stu-id="c4698-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="c4698-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 1 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-132">La topologie de la maille est une liste de correctifs avec 1 point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="c4698-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 2 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-134">La topologie de la maille est une liste de correctifs avec 2 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="c4698-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 3 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-136">La topologie de la maille est une liste de correctifs avec 3 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="c4698-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 4 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-138">La topologie de la maille est une liste de correctifs avec 4 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="c4698-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 5 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-140">La topologie de la maille est une liste de correctifs avec 5 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="c4698-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 6 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-142">La topologie de la maille est une liste de correctifs avec 6 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="c4698-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 7 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-144">La topologie de la maille est une liste de correctifs avec 7 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="c4698-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**\_Topologie primitive \_ 8 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-146">La topologie de la maille est une liste de correctifs avec 8 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="c4698-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 9 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-148">La topologie de la maille est une liste de correctifs avec 9 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="c4698-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**\_Topologie primitive \_ 10 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-150">La topologie de la maille est une liste de correctifs avec 10 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="c4698-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**\_Topologie primitive \_ 11 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-152">La topologie de la maille est une liste de correctifs avec 11 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="c4698-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**\_Topologie primitive \_ 12 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-154">La topologie de la maille est une liste de correctifs avec 12 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="c4698-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**\_Topologie primitive \_ 13 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-156">La topologie de la maille est une liste de correctifs avec 13 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="c4698-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**\_Topologie primitive \_ 14 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-158">La topologie de la maille est une liste de correctifs avec 14 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="c4698-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**\_Topologie primitive \_ 15 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-160">La topologie de la maille est une liste de correctifs avec 15 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="c4698-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**\_Topologie primitive \_ 16 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-162">La topologie de la maille est une liste de correctifs avec 16 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="c4698-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 17 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-164">La topologie de la maille est une liste de correctifs avec 17 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="c4698-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**\_Topologie primitive \_ 18 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-166">La topologie de la maille est une liste de correctifs avec 18 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="c4698-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 19 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-168">La topologie de la maille est une liste de correctifs avec 19 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="c4698-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**\_Topologie primitive \_ 20 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-170">La topologie de la maille est une liste de correctifs avec 20 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="c4698-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 21 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-172">La topologie de la maille est une liste de correctifs avec 21 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="c4698-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**\_Topologie primitive \_ 22 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-174">La topologie de la maille est une liste de correctifs avec 22 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="c4698-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**\_Topologie primitive \_ 23 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-176">La topologie de la maille est une liste de correctifs avec 23 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="c4698-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**\_Topologie primitive \_ 24 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-178">La topologie de la maille est une liste de correctifs avec 24 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="c4698-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive \_ 25 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-180">La topologie de la maille est une liste de correctifs avec 25 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="c4698-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**\_Point de contrôle de topologie primitive \_ 26 \_ \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-182">La topologie de la maille est une liste de correctifs avec 26 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="c4698-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**\_Topologie primitive \_ 27 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-184">La topologie de la maille est une liste de correctifs avec 27 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="c4698-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**\_Topologie primitive \_ 28 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-186">La topologie de la maille est une liste de correctifs avec 28 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="c4698-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**\_Topologie primitive \_ 29 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-188">La topologie de la maille est une liste de correctifs avec 29 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="c4698-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**\_Topologie primitive \_ 30 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-190">La topologie de la maille est une liste de correctifs avec 30 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="c4698-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**\_Topologie primitive \_ 31 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-192">La topologie de la maille est une liste de correctifs avec 31 points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4698-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="c4698-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**\_Topologie PRIMITIVE \_ 32 point de \_ contrôle \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="c4698-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="c4698-194">La topologie de la maille est une liste de correctifs avec des points de contrôle 32.</span><span class="sxs-lookup"><span data-stu-id="c4698-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4698-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4698-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c4698-196">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4698-196">Header</span></span></p></td><td><span data-ttu-id="c4698-197">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c4698-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



