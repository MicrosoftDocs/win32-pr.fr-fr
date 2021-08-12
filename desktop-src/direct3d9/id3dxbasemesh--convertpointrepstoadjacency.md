---
description: Convertit les données représentatives de point en informations d’adjacence de maillage.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'ID3DXBaseMesh :: ConvertPointRepsToAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b888bc7fe8be0aa8bbac1150717ff90440bb797d84d910f7bcb6ee4f35f49345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296207"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a>ID3DXBaseMesh :: ConvertPointRepsToAdjacency, méthode

Convertit les données représentatives de point en informations d’adjacence de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPRep* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau d’une valeur DWORD par vertex de la maille qui contient les données représentatives du point. Ce paramètre est facultatif. Si vous fournissez une valeur **null** , ce paramètre est interprété comme un tableau « Identity ».

</dd> <dt>

*pAdjacency* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille. Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
