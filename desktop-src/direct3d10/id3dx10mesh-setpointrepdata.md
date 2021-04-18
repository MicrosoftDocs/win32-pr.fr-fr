---
description: Définissez les données du point de représentation du maillage.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'ID3DX10Mesh :: SetPointRepData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520336"
---
# <a name="id3dx10meshsetpointrepdata-method"></a>ID3DX10Mesh :: SetPointRepData, méthode

Définissez les données du point de représentation du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPointReps* \[ dans\]
</dt> <dd>

Type : **const [**uint**](../winprog/windows-data-types.md) \***

Données de point REP à définir.

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

 

 
