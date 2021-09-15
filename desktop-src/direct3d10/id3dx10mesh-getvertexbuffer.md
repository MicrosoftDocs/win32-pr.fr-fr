---
description: 'ID3DX10Mesh :: GetVertexBuffer, méthode-récupère la mémoire tampon de vertex associée à la maille.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh :: GetVertexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413251"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>ID3DX10Mesh :: GetVertexBuffer, méthode

Récupère la mémoire tampon de vertex associée à la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iBuffer* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Mémoire tampon de vertex à récupérer. Il s’agit d’une valeur d’index.

</dd> <dt>

*ppVertexBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Mémoire tampon de vertex. Voir [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Spécifications



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

 

 
