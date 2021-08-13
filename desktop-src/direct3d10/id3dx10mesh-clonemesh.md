---
description: Crée un nouveau maillage et le remplit avec les données d’un maillage précédemment chargé.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh :: CloneMesh, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 292522e47dbaf6937d871209006134e866e92fdeb27f6edba4f4f71f6d1fad14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409129"
---
# <a name="id3dx10meshclonemesh-method"></a>ID3DX10Mesh :: CloneMesh, méthode

Crée un nouveau maillage et le remplit avec les données d’un maillage précédemment chargé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Indicateurs de création à appliquer au nouveau maillage. Consultez [**d3dx10 \_ Mesh**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom sémantique pour les données de position.

</dd> <dt>

*pDesc* \[ dans\]
</dt> <dd>

Type : **const [**D3D10 \_ élément d’entrée \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Tableau des \_ structures DESC d’élément d’entrée D3D10 \_ \_ , décrivant le format de vertex pour le maillage retourné. Consultez [**Description de l' \_ \_ élément \_ d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans le tableau pDesc.

</dd> <dt>

*ppCloneMesh* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Nouveau maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
