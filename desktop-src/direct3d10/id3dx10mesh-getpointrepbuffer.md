---
description: Obtient la mémoire tampon du REP du point de la maille.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh :: GetPointRepBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116234"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a>ID3DX10Mesh :: GetPointRepBuffer, méthode

Obtient la mémoire tampon du REP du point de la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppPointReps* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Pointeur vers une mémoire tampon de maillage contenant les données de point du maillage. Consultez [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




