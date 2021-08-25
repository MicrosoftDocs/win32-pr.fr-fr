---
description: Ajoutez des données enfants à la maille.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'ID3DXSaveUserData :: AddMeshChildData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397dc9ade32222dd98e050110811464f6544a1d0af52729417c61fbc3367bdbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893309"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>ID3DXSaveUserData :: AddMeshChildData, méthode

Ajoutez des données enfants à la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshContainer* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Pointeur désignant un conteneur de maillage. Consultez [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pXofSave* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Pointeur vers un objet Save du fichier. x. Utilisez le pointeur pour appeler [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md) pour ajouter un objet de données enfant. N’enregistrez pas les données avec [**ID3DXFileSaveObject :: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Pointeur vers un nœud de données de fichier. x. Utilisez le pointeur pour appeler [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) pour ajouter un objet de données enfant.

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

 

 
