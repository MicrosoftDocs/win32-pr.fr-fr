---
description: Accédez à la mémoire tampon d’adjacence du maillage.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'ID3DX10Mesh :: GetAdjacencyBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535829"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a>ID3DX10Mesh :: GetAdjacencyBuffer, méthode

Accédez à la mémoire tampon d’adjacence du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAdjacency* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Mémoire tampon de contiguïté. Consultez [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




