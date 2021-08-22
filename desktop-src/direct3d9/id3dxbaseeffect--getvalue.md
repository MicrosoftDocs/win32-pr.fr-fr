---
description: Obtient la valeur d’une annotation ou d’un paramètre arbitraire, y compris des types simples, des structs, des tableaux, des chaînes, des nuanceurs et des textures. Cette méthode peut être utilisée à la place de presque tous les appels GetXXX dans ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect :: GetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f957ae3b59f10a086f2326e82478afb6b0ba7fd85bbf6b3f78df5746b7fcb56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494699"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>ID3DXBaseEffect :: GetValue, méthode

Obtient la valeur d’une annotation ou d’un paramètre arbitraire, y compris des types simples, des structs, des tableaux, des chaînes, des nuanceurs et des textures. Cette méthode peut être utilisée à la place de presque tous les appels GetXXX dans [**ID3DXBaseEffect**](id3dxbaseeffect.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ à\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Retourne une mémoire tampon contenant la valeur.

</dd> <dt>

*Octets* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

\[en \] nombre d’octets dans la mémoire tampon. Passez à \_ la passerelle par défaut D3DX si vous savez que votre mémoire tampon est suffisamment grande pour contenir le paramètre entier et que vous souhaitez ignorer la validation de la taille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
