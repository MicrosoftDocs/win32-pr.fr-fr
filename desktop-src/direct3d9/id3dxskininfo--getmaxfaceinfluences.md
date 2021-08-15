---
description: Obtient le nombre maximal d’influences dans un maillage de triangle avec la mémoire tampon d’index spécifiée.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo :: GetMaxFaceInfluences, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84e949c0b6140b4be0f55c47c0f24b3e3b2843009c5c0cd039c76caefa0667a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800668"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>ID3DXSkinInfo :: GetMaxFaceInfluences, méthode

Obtient le nombre maximal d’influences dans un maillage de triangle avec la mémoire tampon d’index spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIB* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Pointeur vers la mémoire tampon d’index qui contient les données d’index de maillage.

</dd> <dt>

*NumFaces* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de visages dans la maille.

</dd> <dt>

*maxFaceInfluences* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers les influences de la face maximale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
