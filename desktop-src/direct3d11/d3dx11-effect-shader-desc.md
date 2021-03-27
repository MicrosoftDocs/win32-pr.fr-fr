---
title: Structure D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Décrit un nuanceur d’effet.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Structure D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870182"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>\_ \_ Structure DESC du nuanceur d’effets D3DX11 \_

Décrit un nuanceur d’effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**pInputSignature**
</dt> <dd>

Type : **const [**Byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Passé dans CreateInputLayout. Valide uniquement sur un nuanceur de sommets ou un nuanceur de géométrie. Consultez [**ID3D11Device :: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**True** si le nuanceur est défini en ligne ; Sinon, **false**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Type : **const [**Byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Bytecode du nuanceur.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Longueur de pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Chaîne de déclaration de flux de sortie (pour le nuanceur Geometry avec SO).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indique le flux pixellisé. Les nuanceurs de géométrie D3D11 peuvent générer jusqu’à quatre flux de données, dont l’un peut être pixellisé.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’entrées dans la signature d’entrée.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’entrées dans la signature de sortie.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’entrées dans la signature de constante de correctif.

</dd> </dl>

## <a name="remarks"></a>Notes

Le \_ \_ nuanceur \_ d’effets D3DX11 DESC est utilisé avec [**ID3DX11EffectShaderVariable :: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

