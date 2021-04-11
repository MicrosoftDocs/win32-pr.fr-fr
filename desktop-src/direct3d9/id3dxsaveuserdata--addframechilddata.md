---
description: Ajoutez des données enfants au frame.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'ID3DXSaveUserData :: AddFrameChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211934"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>ID3DXSaveUserData :: AddFrameChildData, méthode

Ajoutez des données enfants au frame.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFrame* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Pointeur désignant un conteneur de maillage. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofSave* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Pointeur vers un objet Save du fichier. x. Utilisez le pointeur pour appeler [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md) pour ajouter un objet de données enfant. N’enregistrez pas les données avec [**ID3DXFileSaveObject :: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofFrameData* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Pointeur vers un nœud de données de fichier. x. Utilisez le pointeur pour appeler [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) pour ajouter un objet de données enfant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.

## <a name="remarks"></a>Notes

[**ID3DXSaveUserData :: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) et [**ID3DXSaveUserData :: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fournissent un mécanisme d’ajout d’un modèle à un fichier. x pour l’enregistrement des données utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
