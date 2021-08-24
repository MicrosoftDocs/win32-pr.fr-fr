---
description: Pourcentage de temps de traitement des données dans le pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Structure D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676739"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>D3DDEVINFO \_ D3D9PIPELINETIMINGS, structure

Pourcentage de temps de traitement des données dans le pipeline.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé à exécuter des nuanceurs vertex.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé à exécuter des nuanceurs de pixels.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps consacré à l’exécution d’un autre traitement.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps ne traitant rien.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour des performances optimales, il est recommandé de disposer d’une charge équilibrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
