---
description: Demande la désallocation d’un objet conteneur de maillage.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: ID3DXAllocateHierarchy ::D méthode estroyMeshContainer (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921335"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>ID3DXAllocateHierarchy ::D méthode estroyMeshContainer

Demande la désallocation d’un objet conteneur de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshContainerToFree* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Pointeur vers l’objet conteneur de maillage à désallouer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




