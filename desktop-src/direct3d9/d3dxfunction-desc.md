---
description: Décrit une fonction utilisée par un effet.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Structure D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536245"
---
# <a name="d3dxfunction_desc-structure"></a>D3DXFUNCTION \_ desc, structure

Décrit une fonction utilisée par un effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Le nom de la fonction

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Inutilisé. Ce membre sera toujours défini sur zéro par [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
