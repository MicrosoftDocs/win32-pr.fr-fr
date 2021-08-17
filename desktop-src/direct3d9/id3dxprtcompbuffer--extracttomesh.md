---
description: Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer et ajoute les données à un objet ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer :: ExtractToMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 410ec268da89ad4033c88a90c2b37bfa8e78a7b9c229cab72c8ad07e666fce42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730035"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>ID3DXPRTCompBuffer :: ExtractToMesh, méthode

Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumPCA* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de coefficients d’APC à extraire de la mémoire tampon.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descriptions de l’utilisation des sommets de la maille. Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de départ pour les coefficients de l’APC à stocker dans la maille.

</dd> <dt>

*pScene* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) qui stocke les coefficients PCA.

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

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
