---
description: 'ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode-générer une liste de bords de maillage, ainsi qu’une liste des visages qui partagent chaque bord.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55198648be8952f975313dad3019063917eddf4d38f0a7d636039d5802f08e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566939"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode

Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Epsilon* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifie que les vertex qui diffèrent de la position par moins de Epsilon doivent être traités comme coïncidents.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin.

L’ordre des entrées dans la mémoire tampon d’adjacence est déterminé par l’ordre des index de vertex dans le tampon d’index. Le triangle adjacent 0 correspond toujours au bord entre les index des angles 0 et 1. Le triangle 1 adjacent correspond toujours au bord entre les index des angles 1 et 2, tandis que le triangle 2 adjacent correspond au bord entre les index des angles 2 et 0.

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

 

 
