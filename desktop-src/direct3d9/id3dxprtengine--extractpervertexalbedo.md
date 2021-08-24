---
description: Copie les valeurs Albedo par vertex d’une maille.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'ID3DXPRTEngine :: ExtractPerVertexAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e094a7681c13e21cdaab71648b3733749fc179f845e23496a07f3c2b7b99234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747749"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>ID3DXPRTEngine :: ExtractPerVertexAlbedo, méthode

Copie les valeurs Albedo par vertex d’une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers l’objet de maillage [**ID3DXMesh**](id3dxmesh.md) utilisé dans [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) pour créer l’objet [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descriptions de l’utilisation des vertex à copier à partir de la maille. Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*NumChanIn* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de canaux de couleur à copier à partir du maillage. Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
