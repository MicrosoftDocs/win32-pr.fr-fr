---
description: Récupère l’ID de modèle de ce nœud de données de fichier.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'ID3DXFileSaveData :: GetType, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008008"
---
# <a name="id3dxfilesavedatagettype-method"></a>ID3DXFileSaveData :: GetType, méthode

Récupère l’ID de modèle de ce nœud de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Type : **[ **GUID**](guid.md)\***

Pointeur vers le GUID représentant le modèle dans ce nœud de données de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




