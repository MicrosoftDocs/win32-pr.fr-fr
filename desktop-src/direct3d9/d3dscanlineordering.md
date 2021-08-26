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
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987229"
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

## <a name="remarks"></a>Remarques

Cette énumération est utilisée en tant que membre dans [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) et [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




