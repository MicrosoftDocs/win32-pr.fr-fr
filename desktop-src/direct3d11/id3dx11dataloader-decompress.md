---
title: Méthode de décompression ID3DX11DataLoader (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Décompresse les données encodées.'
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
ms.openlocfilehash: 8a4f2424d46748b33918c8b6870c07dbaf4486217f8f3ba7a0a64f881792b81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633029"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader ::D méthode eComPress

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

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

## <a name="remarks"></a>Remarques

Utilisez cette méthode pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.

L' [**interface ID3DX11DataLoader**](id3dx11dataloader.md) peut être héritée et ses membres redéfinis pour prendre en charge des formats de fichier personnalisés.

## <a name="requirements"></a>Configuration requise



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

 

