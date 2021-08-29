---
description: Décrit l’emplacement du fichier include.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Énumération D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: db51cf3c973218096682410ff320c7f46e05051f53616f86ab01bf3b42232124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676059"
---
# <a name="d3dxinclude_type-enumeration"></a>\_Énumération de type D3DXINCLUDE

Décrit l’emplacement du fichier include.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ local**
</dt> <dd>

Recherchez le fichier include dans le projet local.

</dd> <dt>

<span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**\_Système D3DXINC**
</dt> <dd>

Recherchez le fichier include dans le chemin d’accès système.

</dd> <dt>

<span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




