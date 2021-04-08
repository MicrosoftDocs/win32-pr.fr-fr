---
description: Ajoutez un objet de niveau supérieur après la hiérarchie de frames.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'ID3DXSaveUserData :: AddTopLevelDataObjectsPost, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043178"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>ID3DXSaveUserData :: AddTopLevelDataObjectsPost, méthode

Ajoutez un objet de niveau supérieur après la hiérarchie de frames.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pXofSave* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Pointeur vers un objet Save du fichier. x. Utilisez ce pointeur pour appeler [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer l’objet de données à enregistrer. Appelez ensuite [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) pour enregistrer les données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
