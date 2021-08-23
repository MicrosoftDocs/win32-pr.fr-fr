---
description: 'Énumération D3DX10_ERR : les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: Énumération D3DX10_ERR (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b2611bb343801bbe2bd6572f250a7f0eb6d9df7b9980445f1045ee89bee23203
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753569"
---
# <a name="d3dx10_err-enumeration"></a>D3DX10 \_ Err (énumération)

Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées. La liste suivante répertorie les valeurs qui peuvent être retournées par les méthodes incluses dans la bibliothèque de l’utilitaire D3DX. Consultez les descriptions des méthodes individuelles pour obtenir la liste des valeurs que chaque peut retourner. Ces listes ne sont pas nécessairement exhaustives.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ Err \_ ne peut pas \_ modifier le \_ tampon d’index \_**
</dt> <dd>

Le tampon d’index ne peut pas être modifié.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ erreur \_ de \_ maillage non valide**
</dt> <dd>

Le maillage n’est pas valide.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**L' \_ erreur d3dx10 \_ ne peut pas être \_ \_ triée**
</dt> <dd>

L’attribut sort (D3DXMESHOPT \_ ATTRSORT) n’est pas pris en charge en tant que technique d’optimisation.

</dd> <dt>

<span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10 \_ Err de l’erreur \_ \_ non \_ prise en charge**
</dt> <dd>

L’apparence n’est pas prise en charge.

</dd> <dt>

<span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ Err \_ trop \_ grand \_**
</dt> <dd>

Trop d’influences spécifiées.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10 \_ des \_ données non valides \_**
</dt> <dd>

Les données ne sont pas valides.

</dd> <dt>

<span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**La \_ \_ maille chargée d3dx10 Err \_ \_ \_ n’a pas de \_ données**
</dt> <dd>

La maille n’a pas de données.

</dd> <dt>

<span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ Err \_ dupliquer le \_ \_ fragment nommé**
</dt> <dd>

Un fragment portant ce nom existe déjà.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ Err \_ ne peut pas \_ supprimer le \_ dernier \_ élément**
</dt> <dd>

Impossible de supprimer le dernier élément.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le code \_ d’installation FACDD est utilisé pour générer des codes d’erreur, comme dans les macros suivantes.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




