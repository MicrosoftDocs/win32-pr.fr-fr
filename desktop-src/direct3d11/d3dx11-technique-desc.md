---
title: Structure D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Décrit une technique d’effet.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Structure D3DX11_TECHNIQUE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762181"
---
# <a name="d3dx11_technique_desc-structure"></a>Structure de la \_ technique D3DX11 \_ desc

Décrit une technique d’effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nom de cette technique (NULL si non anonyme).

</dd> <dt>

**Mettent**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de passes contenues dans la technique.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’annotations sur cette technique.

</dd> </dl>

## <a name="remarks"></a>Notes

La \_ technique D3DX11 \_ desc est utilisée avec [**ID3DX11EffectTechnique :: GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

