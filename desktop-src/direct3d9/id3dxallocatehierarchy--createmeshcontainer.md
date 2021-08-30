---
description: Demande l’allocation d’un objet conteneur de maillage.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy :: CreateMeshContainer, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fee8b9222358f343b6a8e23435815c8c484a6c8ce86625303e127174d300a197
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026869"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>ID3DXAllocateHierarchy :: CreateMeshContainer, méthode

Demande l’allocation d’un objet conteneur de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nom de la maille.

</dd> <dt>

*pMeshData* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***

Pointeur vers la structure de données de maillage. Consultez [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

*pMaterials* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Tableau de matériaux utilisés dans la maille.

</dd> <dt>

*pEffectInstances* \[ dans\]
</dt> <dd>

Type : **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Tableau d’instances d’effet utilisé dans la maille. Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de matériaux dans le tableau de matériaux.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Tableau d’adjacence pour le maillage.

</dd> <dt>

*pSkinInfo* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

Pointeur vers l’objet de maillage d’apparence si des données d’apparence sont trouvées. Consultez [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

*ppNewMeshContainer* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

Retourne le conteneur de maillage créé. Consultez [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

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

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
