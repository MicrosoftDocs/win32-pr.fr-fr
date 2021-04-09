---
description: Décrit une technique utilisée par un effet.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Structure D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043094"
---
# <a name="d3dxtechnique_desc-structure"></a>D3DXTECHNIQUE \_ desc, structure

Décrit une technique utilisée par un effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Chaîne qui contient le nom de la technique.

</dd> <dt>

**Mettent**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de passes de rendu requises par la technique. Consultez la section Notes.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’annotations. Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Certaines cartes vidéo peuvent restituer deux textures en une seule passe. Toutefois, si une carte n’a pas cette fonctionnalité, il est souvent possible d’afficher le même effet en deux passes, en utilisant une texture pour chaque passe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
