---
description: Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer :: ExtractToMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c838a146a390aa72ac24781ca6f136b028ad41a6ee94fb4210ec4bd3f557acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120613"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>ID3DXPRTBuffer :: ExtractToMesh, méthode

Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumCoefficients* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de coefficients à extraire de la mémoire tampon. Lorsque vous utilisez le transfert luminance précalculé (SH), le nombre de coefficients doit être Order ². La commande doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descriptions de l’utilisation des sommets de la maille. Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de départ pour les coefficients à stocker dans la maille.

</dd> <dt>

*pScene* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) qui stocke les coefficients.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
