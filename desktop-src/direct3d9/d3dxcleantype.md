---
description: Définit les opérations à effectuer sur les vertex en préparation du nettoyage du maillage.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Énumération D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211805"
---
# <a name="d3dxcleantype-enumeration"></a>Énumération D3DXCLEANTYPE

Définit les opérations à effectuer sur les vertex en préparation du nettoyage du maillage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**
</dt> <dd>

Les triangles de fusion qui partagent les mêmes index de vertex mais qui ont des normales de visage pointent dans des directions opposées (triangles de face arrière). À moins que les triangles ne soient pas fractionnés par l’ajout d’un vertex répliqué, les données d’adjacence de maillage des deux triangles peuvent entrer en conflit.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

Si un vertex est l’apex de deux ventilateurs triangulaires (un nœud papillon) et que les opérations de maillage affectent l’un des ventilateurs, vous fractionnez ensuite le vertex partagé en deux nouveaux sommets. Bowties peut provoquer des problèmes pour les opérations telles que la simplification du maillage qui suppriment des vertex, car la suppression d’un vertex affecte deux ensembles distincts de triangles.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN l' \_ apparence**
</dt> <dd>

Utilisez cet indicateur pour empêcher les boucles infinies pendant l’apparence des opérations de maillage d’installation.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Optimisation de D3DXCLEAN \_**
</dt> <dd>

Utilisez cet indicateur pour empêcher les boucles infinies pendant les opérations d’optimisation de maillage.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplification D3DXCLEAN**
</dt> <dd>

Utilisez cet indicateur pour empêcher les boucles infinies pendant les opérations de simplification du maillage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




