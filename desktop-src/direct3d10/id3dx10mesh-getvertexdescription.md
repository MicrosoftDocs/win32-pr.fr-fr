---
description: Accédez à la description du vertex passée dans D3DX10CreateMesh. La description du vertex décrit la disposition des mémoires tampons de vertex du maillage.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh :: GetVertexDescription, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953861"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>ID3DX10Mesh :: GetVertexDescription, méthode

Accédez à la description du vertex passée dans [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La description du vertex décrit la disposition des mémoires tampons de vertex du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDesc* \[ à\]
</dt> <dd>

Type : **const [**D3D10 \_ élément d’entrée \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Tableau d’éléments d’entrée qui décrivent la disposition des mémoires tampons de vertex du maillage. Consultez [**Description de l' \_ \_ élément \_ d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pDeclCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre d’éléments d’entrée dans ppDesc.

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

 

 
