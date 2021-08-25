---
description: Récupère le nom de ce nœud de données de fichier ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'ID3DXFileSaveData :: GetName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7aa6ef69a5296830b2f3bb992fb24ac23fa58adeeea629fd0e1bdeacf6173344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856648"
---
# <a name="id3dxfilesavedatagetname-method"></a>ID3DXFileSaveData :: GetName, méthode

Récupère le nom de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPSTR**](../winprog/windows-data-types.md)**

Adresse d’un pointeur devant recevoir le nom de ce nœud de données de fichier. Si ce paramètre a la **valeur null**, *puiSize* retourne la taille de la chaîne. Si szName pointe vers une mémoire valide, le nom de ce nœud de données de fichier sera copié dans szName jusqu’au nombre de caractères spécifié par *puiSize* .

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Pointeur vers la taille de la chaîne qui représente le nom de ce nœud de données de fichier. Ce paramètre peut avoir la **valeur null** si szName fournit une référence au nom. Ce paramètre retourne la taille de la chaîne si szName a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Remarques

Pour que cette méthode aboutisse, *szName* ou *puiSize* doit être non **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
