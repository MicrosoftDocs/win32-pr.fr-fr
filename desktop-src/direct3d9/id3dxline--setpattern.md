---
description: Applique un modèle de stipple à la ligne.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'ID3DXLine :: SetPattern, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 502fcbc8c3d8a8160ce3390330511d47165493a2bd4cc9a312e5203de7424e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120873"
---
# <a name="id3dxlinesetpattern-method"></a>ID3DXLine :: SetPattern, méthode

Applique un modèle de stipple à la ligne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwPattern* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Décrit le modèle stipple : 1 est opaque, 0 est transparent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
