---
description: Accède aux données du fichier. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData :: Lock, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532188"
---
# <a name="id3dxfiledatalock-method"></a>ID3DXFileData :: Lock, méthode

Accède aux données du fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Pointeur vers la taille des données du fichier. x.

</dd> <dt>

*ppData* \[ dans\]
</dt> <dd>

Type : **const void \* \***

Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet de données de fichier [**ID3DXFileData**](id3dxfiledata.md) . Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Le pointeur *ppData* est uniquement valide pendant un **ID3DXFileData :: Lock** ... Séquence [**ID3DXFileData :: Unlock**](id3dxfiledata--unlock.md) . Vous pouvez effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.

Étant donné qu’il n’est pas garanti que les données de fichier soient correctement alignées avec les limites d’octets, vous devez accéder à *ppData* avec des pointeurs non alignés.

Il n’est pas garanti que les valeurs de paramètre retournées soient valides en raison d’une éventuelle altération de fichier ; par conséquent, votre code doit vérifier les valeurs de paramètre retournées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
