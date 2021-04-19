---
description: Définit les opérations de fusion prises en charge. Consultez la section Notes pour connaître les définitions des termes.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Énumération D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524845"
---
# <a name="d3dblendop-enumeration"></a>Énumération D3DBLENDOP

Définit les opérations de fusion prises en charge. Consultez la section Notes pour connaître les définitions des termes.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Ajouter**
</dt> <dd>

Le résultat est la destination ajoutée à la source. Résultat = source + destination

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ soustraire**
</dt> <dd>

Le résultat est soustrait de la destination à la source. Résultat = source-destination

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**
</dt> <dd>

Le résultat est la source soustraite de la destination. Résultat = source-destination

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ min.**
</dt> <dd>

Le résultat est le minimum de la source et de la destination. Résultat = MIN (source, destination)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**
</dt> <dd>

Le résultat est le maximum de la source et de la destination. Résultat = MAX (source, destination)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

La source, la destination et le résultat sont définis comme suit :



| Terme        | Type   | Description                                                            |
|-------------|--------|------------------------------------------------------------------------|
| Source      | Entrée  | Couleur du pixel source avant l’opération.                        |
| Destination | Entrée  | Couleur du pixel dans la mémoire tampon de destination avant l’opération.     |
| Résultats      | Output | Valeur retournée qui correspond à la couleur fusionnée résultant de l’opération. |



 

Ce type énuméré définit les valeurs utilisées par les États de rendu suivants :

-   D3DRS \_ BLENDOP
-   D3DRS \_ BLENDOPALPHA

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
