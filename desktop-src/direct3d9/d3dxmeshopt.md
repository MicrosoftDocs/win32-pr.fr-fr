---
description: Énumération D3DXMESHOPT-spécifie le type d’optimisation de maillage à effectuer.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Énumération D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d4d26538832a698909ace59da42b13ae51aef93d2d4d622b687f324a62d8361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986489"
---
# <a name="d3dxmeshopt-enumeration"></a>Énumération D3DXMESHOPT

Spécifie le type d’optimisation de maillage à effectuer.

## <a name="syntax"></a>Syntaxe


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ compact**
</dt> <dd>

Réorganise les visages pour supprimer les sommets et les faces inutilisés.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Réorganise les visages pour optimiser le nombre de modifications d’état de groupe d’attributs et les ID3DXBaseMesh améliorées [**::D**](id3dxbasemesh--drawsubset.md) les performances rawsubset.

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Réorganise les visages pour augmenter le taux d’accès au cache des caches de vertex.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Réorganise les visages pour maximiser la longueur des triangles adjacents.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Optimiser les visages uniquement ; n’optimisez pas les vertex.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Lors du tri des attributs, ne fractionnez pas les vertex partagés entre les groupes d’attributs.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**
</dt> <dd>

Affecte la taille du cache de vertex. L’utilisation de cet indicateur spécifie une taille de cache de vertex par défaut qui fonctionne bien sur le matériel hérité.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les \_ indicateurs d’optimisation D3DXMESHOPT STRIPREORDER et D3DXMESHOPT \_ VERTEXCACHE s’excluent mutuellement.

L' \_ indicateur D3DXMESHOPT SHAREVB a été supprimé de cette énumération. utilisez D3DXMESH \_ VB \_ SHARE à la place, dans [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
