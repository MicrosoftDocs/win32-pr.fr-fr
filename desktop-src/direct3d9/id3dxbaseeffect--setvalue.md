---
description: Définir la valeur d’une annotation ou d’un paramètre arbitraire, y compris les types simples, les structs, les tableaux, les chaînes, les nuanceurs et les textures.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect :: SetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116254"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>ID3DXBaseEffect :: SetValue, méthode

Définir la valeur d’une annotation ou d’un paramètre arbitraire, y compris les types simples, les structs, les tableaux, les chaînes, les nuanceurs et les textures.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon qui contient des données.

</dd> <dt>

*Octets* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

\[en \] nombre d’octets dans la mémoire tampon. Passez à \_ la passerelle par défaut D3DX si vous savez que votre mémoire tampon est suffisamment grande pour contenir le paramètre entier et que vous souhaitez ignorer la validation de la taille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Cette méthode peut être utilisée à la place de presque tous les appels d’API de jeu d’effets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
