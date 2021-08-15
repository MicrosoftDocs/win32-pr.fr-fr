---
description: Met à l’échelle tous les échantillons associés à un sous-maillage donné. La méthode est utile pour le calcul de la diffusion sous-surface.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine :: ScaleMeshChunk, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a42046678ef0b44f011c8440cd3456dc9ff236ec0f7a280b4650b49aa53c10d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729583"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>ID3DXPRTEngine :: ScaleMeshChunk, méthode

Met à l’échelle tous les échantillons associés à un sous-maillage donné. La méthode est utile pour le calcul de la diffusion sous-surface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uMeshChunk* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Emplacement dans la maille auquel démarrer les exemples de mise à l’échelle.

</dd> <dt>

*fScale* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur par laquelle multiplier chaque vecteur dans le sous-maillage.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) pour recevoir des échantillons redimensionnés dans le sous-maillage.

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

 

 
