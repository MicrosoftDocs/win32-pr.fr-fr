---
description: Récupère l’ID de modèle dans cet objet de données de fichier.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData :: GetType, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e386c27638ced2be41197bf5f0095a481365dd19bc39b69d5d13d1ac8ec8dc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748529"
---
# <a name="id3dxfiledatagettype-method"></a>ID3DXFileData :: GetType, méthode

Récupère l’ID de modèle dans cet objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PTYPE* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers le GUID représentant le modèle dans cet objet de données de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




