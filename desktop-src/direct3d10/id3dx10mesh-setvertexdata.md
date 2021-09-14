---
description: Définissez les données de vertex dans l’une des mémoires tampons de vertex du maillage.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh :: SetVertexData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922691"
---
# <a name="id3dx10meshsetvertexdata-method"></a>ID3DX10Mesh :: SetVertexData, méthode

Définissez les données de vertex dans l’une des mémoires tampons de vertex du maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iBuffer* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Mémoire tampon de vertex à remplir avec pData.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **const void \***

Données de vertex à définir.

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

 

 
