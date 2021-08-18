---
description: Charger les données de niveau supérieur à partir d’un fichier. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData :: LoadTopLevelData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0ed668657fb0195da7a54bad14d996c06c8fba8f81306491e7be4ce0d97b01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629489"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a>ID3DXLoadUserData :: LoadTopLevelData, méthode

Charger les données de niveau supérieur à partir d’un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

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

 

 




