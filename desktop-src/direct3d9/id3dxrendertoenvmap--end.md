---
description: Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap :: end, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efaf32eb421f6bda38fb922c4a89b1dbbe871842c3b4f07a87ff30c2e6b4dc40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095789"
---
# <a name="id3dxrendertoenvmapend-method"></a>ID3DXRenderToEnvMap :: end, méthode

Restaurez toutes les cibles de rendu et, si nécessaire, composez toutes les faces rendues dans la surface de la carte de l’environnement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison valide d’un ou plusieurs indicateurs [de \_ filtre D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap :: face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
