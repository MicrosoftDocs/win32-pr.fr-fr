---
description: D3DX10CreateMesh fonction-crée un objet de maillage à l’aide d’un déclarateur.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh, fonction (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4f044d3337a2da05eb78b027492b870f450e4309c94faa8c72db935437511dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853479"
---
# <a name="d3dx10createmesh-function"></a>D3DX10CreateMesh fonction)

Crée un objet de maillage à l’aide d’un déclarateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers une [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), l’objet appareil à associer à la maille.

</dd> <dt>

*pDeclaration* \[ dans\]
</dt> <dd>

Type : **const [**D3D10 \_ élément d’entrée \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Tableau d’éléments de [**\_ \_ \_ Description d’élément d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , décrivant le format de vertex pour le maillage retourné. Ce paramètre doit être directement mappé à un format de vertex flexible.

</dd> <dt>

*DeclCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Sémantique qui identifie la partie de la déclaration de vertex qui contient des informations de position.

</dd> <dt>

*VertexCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex pour le maillage. Ce paramètre doit être supérieur à 0.

</dd> <dt>

*FaceCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de faces de la maille. La plage valide pour ce nombre est supérieure à 0, et une valeur inférieure à la valeur DWORD maximale (généralement 65534), car le dernier index est réservé.

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs à partir de la [**\_ maille d3dx10**](d3dx10-mesh.md), en spécifiant des options pour le maillage.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Adresse d’un pointeur vers une [**interface ID3DX10Mesh**](id3dx10mesh.md)représentant l’objet de maillage créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX, fonctions](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
