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
ms.openlocfilehash: 2266737a04b28940eeaa3758f5bd3909ec815745cb060836c499cfd4b3142266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124924"
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

## <a name="remarks"></a>Remarques

La \_ technique D3DX11 \_ desc est utilisée avec [**ID3DX11EffectTechnique :: GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

