---
title: Structure D3DX11_PASS_DESC (D3dx11effect. h)
description: Décrit une passe d’effet, qui contient l’état du pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Structure D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982551"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11, structure de la \_ passe \_ desc

Décrit une passe d’effet, qui contient l’état du pipeline.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nom de cette passe (**null** si non anonyme).

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’annotations sur cette passe.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Signature du nuanceur de sommets ou du nuanceur de géométrie (s’il n’existe aucun nuanceur de vertex) ou **null** s’il n’en existe pas.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Taille de singature en octets.

</dd> <dt>

**StencilRef**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur de référence de stencil utilisée dans l’état de stencil de profondeur.

</dd> <dt>

**SampleMask**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Exemple de masque pour l’état de fusion.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Facteurs de mélange par composant (RVBA) pour l’état de fusion.

</dd> </dl>

## <a name="remarks"></a>Notes

D3DX11 \_ Pass \_ desc est utilisé avec [**ID3DX11EffectPass :: GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

