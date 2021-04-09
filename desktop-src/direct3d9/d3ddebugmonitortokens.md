---
description: Définit les jetons du moniteur de débogage.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Énumération D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953814"
---
# <a name="d3ddebugmonitortokens-enumeration"></a>Énumération D3DDEBUGMONITORTOKENS

Définit les jetons du moniteur de débogage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ activer**
</dt> <dd>

Activez le moniteur de débogage.

</dd> <dt>

<span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**Désactivation de D3DDMT \_**
</dt> <dd>

Désactivez le moniteur de débogage.

</dd> <dt>

<span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS DEBUGMONITORTOKEN et ne sont pertinentes que pour les versions Debug.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
