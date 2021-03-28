---
title: Structure D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Décrit une passe d’effet.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Structure D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982546"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>\_ \_ Structure DESC du nuanceur de passe D3DX11 \_

Décrit une passe d’effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**pShaderVariable**
</dt> <dd>

Type : **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Variable dont provient ce nuanceur.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Élément de pShaderVariable (si un tableau) ou 0 s’il n’est pas applicable.

</dd> </dl>

## <a name="remarks"></a>Notes

Le \_ \_ nuanceur \_ de passe D3DX11 DESC est utilisé avec les méthodes [**ID3DX11EffectPass**](id3dx11effectpass.md) \* ShaderDesc.

S’il s’agit d’une assignation de nuanceur Inline, l’interface retournée est une variable de nuanceur anonyme, qui ne peut pas être récupérée d’une autre façon. Son nom dans la description de la variable est « $Anonymous ». S’il n’y a aucune assignation de ce type dans le bloc de réussite, pShaderVariable ! = **null**, mais pShaderVariable->IsValid () = = **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

