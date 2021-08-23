---
description: Retourne l’index de l’échantillonneur.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'ID3DXConstantTable :: GetSamplerIndex, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dac22cc15e93198e7d494986b2279ae7e1d11fdb3c8cb65b3caddf9b905595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987569"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>ID3DXConstantTable :: GetSamplerIndex, méthode

Retourne l’index de l’échantillonneur.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ à\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de l’échantillonneur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Retourne le numéro d’index de l’échantillonneur à partir de la table constante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
