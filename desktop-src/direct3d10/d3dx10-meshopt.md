---
description: 'Énumération D3DX10_MESHOPT : spécifie le type d’optimisation de maillage à effectuer.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Énumération D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105447"
---
# <a name="d3dx10_meshopt-enumeration"></a>D3DX10 \_ MESHOPT, énumération

Spécifie le type d’optimisation de maillage à effectuer.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ compact**
</dt> <dd>

Réorganise les visages pour supprimer les sommets et les faces inutilisés.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ attr \_ sort**
</dt> <dd>

Réorganise les visages pour optimiser le nombre de modifications d’état de groupe d’attributs et les performances améliorées de DrawSubset.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**\_Cache de \_ vertex d3dx10 MESHOPT \_**
</dt> <dd>

Réorganise les visages pour augmenter le taux d’accès au cache des caches de vertex.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Réorganisation de la \_ bande d3dx10 MESHOPT \_ \_**
</dt> <dd>

Réorganise les visages pour maximiser la longueur des triangles adjacents.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignorer les \_ basculements**
</dt> <dd>

Optimiser les visages uniquement ; n’optimisez pas les vertex.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ ne \_ pas \_ fractionner**
</dt> <dd>

Lors du tri des attributs, ne fractionnez pas les vertex partagés entre les groupes d’attributs.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ appareil \_ indépendant**
</dt> <dd>

Affecte la taille du cache de vertex. L’utilisation de cet indicateur spécifie une taille de cache de vertex par défaut qui fonctionne bien sur le matériel hérité.

</dd> </dl>

## <a name="remarks"></a>Notes 

Les \_ indicateurs d’optimisation D3DXMESHOPT STRIPREORDER et D3DXMESHOPT \_ VERTEXCACHE s’excluent mutuellement.

L' \_ indicateur D3DXMESHOPT SHAREVB a été supprimé de cette énumération. Utilisez le \_ partage VB D3DXMESH \_ à la place, dans D3DXMESH.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




