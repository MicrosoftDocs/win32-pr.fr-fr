---
description: Définissez les données d’adjacence du maillage.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'ID3DX10Mesh :: SetAdjacencyData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8e183fb6fad07b92d8bca15654456ca1d31a11839af033222803044f8207a14f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990379"
---
# <a name="id3dx10meshsetadjacencydata-method"></a>ID3DX10Mesh :: SetAdjacencyData, méthode

Définissez les données d’adjacence du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**uint**](../winprog/windows-data-types.md) \***

Données d’adjacence à définir.

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

 

 
