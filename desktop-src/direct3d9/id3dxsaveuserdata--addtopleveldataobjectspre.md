---
description: Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'ID3DXSaveUserData :: AddTopLevelDataObjectsPre, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52052a24c34c99260a68cd5cdeaa7487e6b71c086ac30922a06de241de8319ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801159"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>ID3DXSaveUserData :: AddTopLevelDataObjectsPre, méthode

Ajoutez un objet de niveau supérieur avant la hiérarchie des frames.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddTopLevelDataObjectsPre(
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

 

 
