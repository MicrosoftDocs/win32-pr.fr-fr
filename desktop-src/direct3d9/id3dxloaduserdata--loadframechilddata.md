---
description: Charger les données enfants d’un frame à partir d’un fichier. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'ID3DXLoadUserData :: LoadFrameChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3dcb9fa8218804b0d6fdb5532dd54bc2b2b4a3921ea4462692a36e671efb404d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802179"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>ID3DXLoadUserData :: LoadFrameChildData, méthode

Charger les données enfants d’un frame à partir d’un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrame* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)**

Pointeur désignant un conteneur de maillage. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofChildData* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Pointeur vers une structure de données de fichier. x. Cela est défini dans dxfile. h.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




