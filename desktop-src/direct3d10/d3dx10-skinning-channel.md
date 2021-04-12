---
description: Membre de la déclaration de vertex sur laquelle effectuer l’apparence de logiciel. Utilisé avec l’API ID3DX10SkinInfo ::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Structure D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211822"
---
# <a name="d3dx10_skinning_channel-structure"></a>Structure de canal d' \_ apparence d3dx10 \_

Membre de la déclaration de vertex sur laquelle effectuer l’apparence de logiciel. Utilisé avec l’API [**ID3DX10SkinInfo ::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Membres

<dl> <dt>

**SrcOffset**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de chaque vertex source.

</dd> <dt>

**DestOffset**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset à partir du début de chaque vertex de destination.

</dd> <dt>

**IsNormal**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Détermine le tableau de matrices à utiliser dans l’API [**ID3DX10SkinInfo ::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) . Si la valeur est true, *pInverseTransposeBoneMatrices* est utilisé ; sinon, *pBoneMatrices* est utilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
