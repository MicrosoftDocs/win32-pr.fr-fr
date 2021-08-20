---
title: Structure D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Décrit un effet.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Structure D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989989"
---
# <a name="d3dx11_effect_desc-structure"></a>\_ \_ Structure DESC de l’effet D3DX11

Décrit un effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de mémoires tampons constantes dans cet effet.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de variables globales dans cet effet.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’interfaces globales dans cet effet.

</dd> <dt>

**Technologie**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de techniques dans cet effet.

</dd> <dt>

**Groupes**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de groupes dans cet effet.

</dd> </dl>

## <a name="remarks"></a>Remarques

L' \_ effet D3DX11 \_ desc est utilisé avec [**ID3DX11Effect :: GetDesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

