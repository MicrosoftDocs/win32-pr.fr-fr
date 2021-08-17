---
description: Spécifie comment combiner les données de glyphe des surfaces source et de destination dans un appel à ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Énumération D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8d968770eb58d9d3dd59f178b05e8e6536079e8de601ddef602a41da4b52ee51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911167"
---
# <a name="d3dcomposerectsop-enumeration"></a>Énumération D3DCOMPOSERECTSOP

Spécifie comment combiner les données de glyphe des surfaces source et de destination dans un appel à [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**\_Copie D3DCOMPOSERECTS**
</dt> <dd>

Copiez la source vers la destination.

</dd> <dt>

<span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ ou**
</dt> <dd>

Au niveau du bit ou de la source et de la destination.

</dd> <dt>

<span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ et**
</dt> <dd>

Au niveau du bit et de la source et de la destination.

</dd> <dt>

<span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ nég**
</dt> <dd>

Copiez la source négative vers la destination (DST & ~ SRC).

</dd> <dt>

<span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ forcer \_ DWORD**
</dt> <dd>

Réservé. Utilisé pour forcer l’énumération à une taille de 32 bits.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




