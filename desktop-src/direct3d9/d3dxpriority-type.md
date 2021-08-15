---
description: Définit le type de priorité auquel une piste d’animation est assignée.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Énumération D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: e7ea5b7447b896c6b582280216af4d6c05cc540286ad31a2bfb337975fe6c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524848"
---
# <a name="d3dxpriority_type-enumeration"></a>\_Énumération de type D3DXPRIORITY

Définit le type de priorité auquel une piste d’animation est assignée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ bas**
</dt> <dd>

La piste doit être fusionnée avec toutes les pistes de faible priorité avant que la fusion basse priorité ne soit mélangée avec la fusion haute priorité.

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ élevé**
</dt> <dd>

La piste doit être fusionnée avec toutes les pistes haute priorité avant que la fusion haute priorité ne soit mélangée à la fusion basse priorité.

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les pistes avec la même priorité sont fusionnées ensemble, et les deux valeurs résultantes sont ensuite fusionnées à l’aide du facteur de fusion de priorité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




