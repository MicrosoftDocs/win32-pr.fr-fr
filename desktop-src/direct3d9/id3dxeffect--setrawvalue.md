---
description: Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect :: SetRawValue, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543768"
---
# <a name="id3dxeffectsetrawvalue-method"></a>ID3DXEffect :: SetRawValue, méthode

Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de la valeur à définir, ou nom de la valeur transmise en tant que chaîne. Le passage d’un handle est plus efficace. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **void \***

Pointeur vers une mémoire tampon qui contient les données à définir. SetRawValue vérifie la présence de mémoire valide, mais n’effectue aucune vérification des données valides.

</dd> <dt>

*OffsetInBytes* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre d’octets entre le début des données d’effet et le début des constantes d’effet que vous allez définir.

</dd> <dt>

*Octets* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Taille de la mémoire tampon à définir, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : E \_ INVALIDCALL.

## <a name="remarks"></a>Notes

SetRawValue est un moyen très rapide de définir des constantes d’effet, car il effectue une copie de mémoire sans effectuer de validation ou de conversion de données (comme la conversion d’une matrice de lignes principales en colonne-matrice principale). Utilisez SetRawValue pour définir une série de constantes à effet contigu. Par exemple, vous pouvez définir un tableau de vingt matrices avec 20 appels à [**ID3DXBaseEffect :: SetMatrix**](id3dxbaseeffect--setmatrix.md) ou à l’aide d’un SetRawValue unique.

Toutes les valeurs sont supposées être matrix4x4s ou float4s et toutes les matrices sont supposées être dans l’ordre colonne-principal. Les valeurs int ou float sont converties en float4 ; par conséquent, il est fortement recommandé d’utiliser SetRawValue avec uniquement des données float4 ou matrix4x4.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
