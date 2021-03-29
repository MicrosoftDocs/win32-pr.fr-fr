---
title: Structure D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Décrit une variable Effect.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Structure D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996205"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>Structure de la \_ variable d’effet D3DX11 \_ \_

Décrit une variable Effect.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nom de cette variable, annotation ou membre de structure.

</dd> <dt>

**Équivalent**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Chaîne sémantique de ce membre de la variable ou de la structure (NULL pour les annotations ou s’il n’est pas présent).

</dd> <dt>

**Indicateurs**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indicateurs facultatifs pour les variables d’effet.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’annotations sur cette variable (toujours 0 pour les annotations).

</dd> <dt>

**BufferOffset**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Offset dans qui contient CBuffer ou tbuffer (toujours 0 pour les annotations ou les variables qui ne sont pas dans des mémoires tampons constantes).

</dd> <dt>

**ExplicitBindPoint**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Utilisé si la variable a été explicitement liée à l’aide du mot clé Register. Vérifiez les indicateurs pour \_ le \_ \_ point de \_ liaison explicite \_ de la variable d’effet D3DX11.

</dd> </dl>

## <a name="remarks"></a>Notes

La \_ \_ variable d’effet D3DX11 \_ desc est utilisée avec [**ID3DX11EffectVariable :: GetDesc**](id3dx11effectvariable-getdesc.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

