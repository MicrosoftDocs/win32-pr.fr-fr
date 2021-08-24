---
description: Les applications utilisent les méthodes de l’interface ID3DXSkinInfo pour manipuler les matrices osseuses, qui sont utilisées pour l’apparence des données de vertex pour l’animation. Cette interface n’est plus strictement liée à ID3DXMesh et peut être utilisée pour envelopper n’importe quel jeu de données de vertex.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interface ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727759"
---
# <a name="id3dxskininfo-interface"></a>Interface ID3DXSkinInfo

Les applications utilisent les méthodes de l’interface ID3DXSkinInfo pour manipuler les matrices osseuses, qui sont utilisées pour l’apparence des données de vertex pour l’animation. Cette interface n’est plus strictement liée à [**ID3DXMesh**](id3dxmesh.md) et peut être utilisée pour envelopper n’importe quel jeu de données de vertex.

## <a name="members"></a>Membres

L’interface **ID3DXSkinInfo** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSkinInfo** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXSkinInfo** possède ces méthodes.



| Méthode                                                                              | Description                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](id3dxskininfo--clone.md)                                               | Clone un objet d’informations d’apparence.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Prend un maillage et retourne un nouveau maillage avec des poids de fusion par vertex et une table de combinaisons de segments. Le tableau décrit les segments qui affectent les sous-ensembles de la maille.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Prend une maille et retourne un nouveau maillage avec des poids de fusion par vertex, des index et une table de combinaisons de segments. Le tableau décrit les palettes osseuses qui affectent les sous-ensembles de la maille.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Récupère l’index de l’influence osseuse affectant un seul vertex.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Obtient les vertex et les poids influencés par un segment.<br/>                                                                                                                               |
| [**GetBoneName**](id3dxskininfo--getbonename.md)                                   | Obtient le nom du segment à partir de l’index de l’OS.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Obtient la matrice de décalage de l’OS.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Récupère le facteur de fusion et le vertex affectés par une influence osseuse spécifiée.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Obtient la déclaration de vertex.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Obtient la valeur de vertex de fonction fixe.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Obtient le nombre maximal d’influences dans un maillage de triangle avec la mémoire tampon d’index spécifiée.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Obtient le nombre maximal d’influences pour un vertex de la maille.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Obtient l’influence osseuse minimale. Les valeurs d’influence inférieures à cette valeur sont ignorées.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Obtient le nombre d’influences pour un segment.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Obtient le nombre d’os.<br/>                                                                                                                                                           |
| [**Mappe**](id3dxskininfo--remap.md)                                               | Met à jour les informations d’influence osseuse pour qu’elles correspondent aux sommets après leur réorganisation. Cette méthode doit être appelée si la mémoire tampon de vertex cible a été réorganisée en externe.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Définit la valeur d’influence d’un segment.<br/>                                                                                                                                                |
| [**SetBoneName**](id3dxskininfo--setbonename.md)                                   | Définit le nom du segment.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Définit la matrice de décalage de l’OS.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Définit une valeur d’influence d’un segment sur un seul vertex.<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | Définit la déclaration de vertex.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Définit le type de format de vertex flexible.<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Définit l’influence minimale du segment. Les valeurs d’influence inférieures à cette valeur sont ignorées.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Applique les enveloppes logicielles aux vertex cibles en fonction des matrices actuelles.<br/>                                                                                                     |



 

## <a name="remarks"></a>Remarques

Créez une interface **ID3DXSkinInfo** avec [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)ou [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Le type LPD3DXSKININFO est défini comme un pointeur vers l’interface **ID3DXSkinInfo** .


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
