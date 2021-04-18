---
description: Utilisé pour décompresser des données encodées. En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader ::D méthode eComPress (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523189"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader ::D méthode eComPress

Utilisé pour décompresser des données encodées. En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.

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

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Taille des données vers lesquelles pointe ppData.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

L' [**interface ID3DX10DataLoader**](id3dx10dataloader.md) peut être héritée et ses membres redéfinis. La décompression peut être redéfinie pour prendre en charge vos propres formats de fichier personnalisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
