---
title: Méthode de décompression ID3DX11DataLoader (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Décompresse les données encodées.'
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Méthode de décompression Direct3D 11
- Méthode de décompression Direct3D 11, interface ID3DX11DataLoader
- ID3DX11DataLoader interface, méthode de décompression Direct3D 11
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954008"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader ::D méthode eComPress

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Décompresse les données encodées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppData* \[ à\]
</dt> <dd>

Type : **void \* \***

Pointeur vers les données brutes à décompresser.

</dd> <dt>

*pcBytes* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Taille des données vers lesquelles pointe ppData.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Utilisez cette méthode pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.

L' [**interface ID3DX11DataLoader**](id3dx11dataloader.md) peut être héritée et ses membres redéfinis pour prendre en charge des formats de fichier personnalisés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

