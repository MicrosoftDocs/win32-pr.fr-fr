---
description: Prépare un appareil pour le dessin de lignes.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine :: Begin, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542193"
---
# <a name="id3dxlinebegin-method"></a>ID3DXLine :: Begin, méthode

Prépare un appareil pour le dessin de lignes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

L’appel de **ID3DXLine :: Begin** est facultatif. Si elle est appelée en dehors d’une séquence ID3DXLine :: Begin/ID3DXLine :: end, les fonctions de dessin appellent en interne ID3DXLine :: Begin et ID3DXLine :: end. Pour éviter une surcharge supplémentaire, cette méthode doit être utilisée si plusieurs fonctions de dessin seront appelées successivement.

Cette méthode doit être appelée à partir d’une séquence [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) et [**IDirect3DDevice9 :: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

ID3DXLine :: Begin ne peut pas être utilisé comme substitut pour [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
