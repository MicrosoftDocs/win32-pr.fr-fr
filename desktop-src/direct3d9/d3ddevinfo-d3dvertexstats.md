---
description: Signale le nombre de triangles qui ont été traités et découpés par le traitement du vertex logiciel du Runtime.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: Structure D3DDEVINFO_D3DVERTEXSTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3baa6738e5d90d2353beb6c7d7bf0ab85770af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522581"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>D3DDEVINFO \_ D3DVERTEXSTATS, structure

Signale le nombre de triangles qui ont été traités et découpés par le traitement du vertex logiciel du Runtime.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre total de triangles qui ne sont pas découpés dans ce frame.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de nouveaux triangles générés par le découpage.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez le runtime de débogage et le traitement du vertex logiciel pour obtenir le nombre de primitives non découpées et découpées pour une scène particulière. Les primitives sont généralement découpées en fonction d’une bande de protection (le cas échéant). La bande de protection du découpage est définie avec des paramètres tels que GuardBandLeft dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
