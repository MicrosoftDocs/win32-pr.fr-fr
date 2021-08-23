---
description: Obtient le nombre de vertex dans la maille.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh :: GetVertexCount, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566889"
---
# <a name="id3dx10meshgetvertexcount-method"></a>ID3DX10Mesh :: GetVertexCount, méthode

Obtient le nombre de vertex dans la maille. Un maillage peut contenir plusieurs mémoires tampons de vertex (c’est-à-dire qu’une mémoire tampon de vertex peut contenir toutes les données de position, une autre peut contenir toutes les données de coordonnée de texture, etc.), mais chaque mémoire tampon de vertex contiendra le même nombre d’éléments.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex dans la maille.

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

 

 
