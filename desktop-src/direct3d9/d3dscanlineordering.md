---
description: Indicateurs spécifiant la méthode utilisée par le rastériseur pour créer une image sur une surface.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Énumération D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535209"
---
# <a name="d3dscanlineordering-enumeration"></a>Énumération D3DSCANLINEORDERING

Indicateurs spécifiant la méthode utilisée par le rastériseur pour créer une image sur une surface.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressif**
</dt> <dd>

L’image est créée à partir du premier numérisation jusqu’au dernier sans ignorer les autres.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ entrelacé**
</dt> <dd>

L’image est créée à l’aide de la méthode entrelacée dans laquelle les lignes portant un numéro impair sont dessinées sur les passes impaires, et les lignes paires sont dessinées sur les passes paires.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée en tant que membre dans [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) et [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




