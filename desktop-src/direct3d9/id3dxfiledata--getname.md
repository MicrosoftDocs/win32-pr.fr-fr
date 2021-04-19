---
description: Récupère le nom de cet objet de données de fichier.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData :: GetName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522370"
---
# <a name="id3dxfiledatagetname-method"></a>ID3DXFileData :: GetName, méthode

Récupère le nom de cet objet de données de fichier.

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

Adresse d’un pointeur devant recevoir le nom de cet objet de données de fichier. Si ce paramètre a la **valeur null**, puiSize retourne la taille de la chaîne. Si szName pointe vers une mémoire valide, le nom de cet objet de données de fichier sera copié dans szName jusqu’au nombre de caractères spécifié par puiSize.

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Pointeur vers la taille de la chaîne qui représente le nom de cet objet de données de fichier. Ce paramètre peut avoir la **valeur null** si szName fournit une référence au nom. Ce paramètre retourne la taille de la chaîne si szName a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Pour que cette méthode aboutisse, szName ou *puiSize* doit être non **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
