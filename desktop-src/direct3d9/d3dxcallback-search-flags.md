---
description: Indicateurs utilisés pour obtenir des informations de rappel.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Énumération D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043120"
---
# <a name="d3dxcallback_search_flags-enumeration"></a>\_Énumération d’indicateurs de recherche D3DXCALLBACK \_

Indicateurs utilisés pour obtenir des informations de rappel.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK la \_ recherche à \_ l’exception de la \_ \_ position initiale**
</dt> <dd>

Exclut les rappels situés à la position initiale de la recherche.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ recherche \_ derrière \_ la \_ position initiale**
</dt> <dd>

Inversez le sens de la recherche de rappel.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK de \_ force de recherche de \_ \_ mot de passe**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




