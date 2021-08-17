---
description: Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData :: RegisterTemplates, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a41a43f8f319ee09f24c4f62092e4718773dc312cb7886b0fc7c95781e614c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628729"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>ID3DXSaveUserData :: RegisterTemplates, méthode

Rappel permettant à l’utilisateur d’inscrire un modèle de fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pXFileApi* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXFILE**](id3dxfile.md)**

Utilisez ce pointeur pour inscrire des modèles de fichier. x définis par l’utilisateur. Consultez [**ID3DXFile**](id3dxfile.md). N’utilisez pas ce paramètre pour ajouter des objets de données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.

## <a name="remarks"></a>Remarques

**ID3DXSaveUserData :: RegisterTemplates** et [**ID3DXSaveUserData :: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fournissent un mécanisme d’ajout d’un modèle à un fichier. x pour l’enregistrement des données utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
