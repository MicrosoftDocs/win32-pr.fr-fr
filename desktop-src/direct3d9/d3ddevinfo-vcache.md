---
description: Indicateurs d’optimisation du cache de vertex.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Structure D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e065c981cc42db6adbad8cfa7a14e415712aae74942e9f3aab3ecb0b353f5ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894499"
---
# <a name="d3ddevinfo_vcache-structure"></a>D3DDEVINFO \_ Vcache, structure

Indicateurs d’optimisation du cache de vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Modèle**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Modèle binaire. La valeur de retour doit être le FOURCC ('C', 'A', 'C', 'H').

</dd> <dt>

**OptMethod**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Méthode Optimizations. Utilisez 0 pour récupérer les bandes les plus longues. Utilisez 1 pour optimiser l’utilisation du cache de vertex.

</dd> <dt>

**CacheSize**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille du cache utilisée comme cible pour l’optimisation. Cela est requis uniquement si OptMethod est 1.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Utilisé par les méthodes d’optimisation internes pour déterminer le moment du redémarrage des bandes. Cela ne peut pas être défini ou modifié par un utilisateur. Cela est requis uniquement si OptMethod est 1.

</dd> </dl>

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

 

 
