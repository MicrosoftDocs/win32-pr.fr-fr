---
description: Comment le pipeline interprète les données de vertex qui sont liées à l’étape assembleur d’entrée. Ces valeurs de topologie primitives déterminent la façon dont les données de vertex sont restituées à l’écran.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Énumération de la topologie primitive d3d11 \_'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 7c899d738b2a80036eaea61352f5e8aa82c73ddbeb48433d275d74506a478d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990009"
---
# <a name="d3d11_primitive_topology-enumeration"></a>\_Énumération de la topologie primitive d3d11 \_

Comment le pipeline interprète les données de vertex qui sont liées à l’étape assembleur d’entrée. Ces valeurs de topologie primitives déterminent la façon dont les données de vertex sont restituées à l’écran.

## <a name="syntax"></a>Syntaxe


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologie primitive d3d11 \_ \_ non définie**
</dt> <dd>

L’étape IA n’a pas été initialisée avec une topologie primitive. L’étape IA ne fonctionnera pas correctement, sauf si une topologie primitive est définie.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**\_Topologie primitive d3d11 \_ \_ POINTLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de points.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Topologie primitive d3d11 \_ \_ LINELIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de lignes.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_Topologie primitive d3d11 \_ \_ LINESTRIP**
</dt> <dd>

Interpréter les données de vertex comme une bande de courbes.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_Topologie primitive d3d11 \_ \_ TRIANGLELIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de triangles.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_Topologie primitive d3d11 \_ \_ TRIANGLESTRIP**
</dt> <dd>

Interpréter les données de vertex comme une bande triangulaire.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ primitive \_ \_ LINELIST \_ adj**
</dt> <dd>

Interpréter les données de vertex comme une liste de lignes avec des données d’contiguïté.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ primitive \_ \_ LINESTRIP \_ adj**
</dt> <dd>

Interpréter les données de vertex comme une bande de lignes avec des données d’adjacence.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ primitive \_ \_ TRIANGLELIST \_ adj**
</dt> <dd>

Interpréter les données de vertex comme une liste de triangles avec les données d’contiguïté.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ primitive \_ \_ TRIANGLESTRIP \_ adj**
</dt> <dd>

Interpréter les données de vertex comme une bande triangulaire avec des données d’contiguïté.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 1 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 2 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 3 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 4 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 5 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 6 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 7 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 8 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 9 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 10 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 11 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 12 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 13 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 14 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 15 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 16 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 17 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**\_Topologie primitive d3d11- \_ point de \_ \_ contrôle 18 \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 19 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 20 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ primitive primitive \_ \_ 21 point \_ de \_ contrôle \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 22 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ primitive de la \_ topologie de point de \_ \_ contrôle 23 \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 24 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ primitive \_ PATCHLIST, \_ \_ point de contrôle 25 \_ \_**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**\_Point de contrôle de topologie d3d11 primitive \_ \_ 26 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**POINT de contrôle de la \_ topologie primitive d3d11 \_ \_ 27 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 28 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 29 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 30 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**\_Topologie primitive d3d11 \_ \_ 31 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**\_Topologie primitive D3D11 \_ \_ 32 point de \_ contrôle \_ \_ PATCHLIST**
</dt> <dd>

Interpréter les données de vertex comme une liste de correctifs.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’énumération de la **\_ \_ topologie primitive d3d11** est de type défini dans le fichier d’en-tête d3d11. h comme une ÉNUMÉRation de la topologie de la [**\_ primitive \_ D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , qui est entièrement définie dans le fichier d’en-tête D3DCommon. h.
