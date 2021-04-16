---
description: Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Structure D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530867"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>D3DDEVINFO \_ D3D9CACHEUTILIZATION, structure

Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Taux d’accès pour la recherche d’une texture dans le cache de texture. Cela suppose qu’il existe un cache de texture. L’amélioration du niveau de détail pour utiliser la texture la plus détaillée, l’utilisation de nombreuses textures volumineuses ou la génération d’un modèle d’accès de texture presque aléatoire sur les textures volumineuses avec un code de nuanceur personnalisé peut avoir un impact considérable sur le taux d’accès au cache de texture.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Taux d’accès pour la recherche des vertex transformés dans le cache de vertex. Le GPU est conçu pour transformer des vertex indexés et peut les stocker dans un cache de vertex. Si vous utilisez des mailles, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) ou [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) peut entraîner une meilleure utilisation du cache de vertex.

</dd> </dl>

## <a name="remarks"></a>Notes

Un cache efficace est généralement plus proche d’un taux d’accès de 90% et un cache inefficace est généralement plus proche d’un taux d’accès de 10% (même si un faible pourcentage n’est pas nécessairement un problème).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
