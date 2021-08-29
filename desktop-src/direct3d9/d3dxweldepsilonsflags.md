---
description: Options de soudure conjointe des sommets.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Énumération D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: c206718cd55a05d67d0a38d90c254238b63e964fa1f26149e75b57e09db359e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044487"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>Énumération D3DXWELDEPSILONSFLAGS

Options de soudure conjointe des sommets.

## <a name="syntax"></a>Syntaxe


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**
</dt> <dd>

Soudure ensemble tous les vertex qui se trouvent au même emplacement. L’utilisation de cet indicateur évite une comparaison Epsilon entre les composants de vertex.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**
</dt> <dd>

Si un composant de vertex donné se trouve dans Epsilon, modifiez les vertex partiellement correspondants afin que les deux composants soient identiques. Si tous les composants sont identiques, supprimez l’un des sommets.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**
</dt> <dd>

Indique à la soudure d’autoriser uniquement les modifications apportées aux vertex et non la suppression. Cet indicateur n’est valide que si D3DXWELDEPSILONS \_ WELDPARTIALMATCHES est défini. Il est utile de modifier les vertex pour qu’ils soient égaux, mais pas pour permettre la suppression des vertex.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**
</dt> <dd>

Indique à la soudure de ne pas fractionner les vertex qui se trouvent dans des groupes d’attributs distincts. Lorsque la méthode [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) est appelée avec l' \_ indicateur D3DXMESHOPT ATTRSORT, l’indicateur D3DXMESHOPT \_ DONOTSPLIT est également défini. La définition de cet indicateur peut ralentir le traitement des vertex logiciels.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




