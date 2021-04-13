---
description: ID3DX10SkinInfo vous permet d’optimiser, de traiter et de définir manuellement la relation entre les segments et les vertex de vos mailles (voir animation de squelette sur Wikipédia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interface ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322949"
---
# <a name="id3dx10skininfo-interface"></a>Interface ID3DX10SkinInfo

ID3DX10SkinInfo vous permet d’optimiser, de traiter et de définir manuellement la relation entre les segments et les vertex de vos mailles (voir [animation de squelette sur Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)). Il est particulièrement utile pour créer des fichiers. x exportés par des applications DCC (telles que 3DS Max et Maya) plus compatibles avec le matériel et pour améliorer la vitesse de rendu de vos mailles dépouillées en mode de rendu logiciel.

## <a name="members"></a>Membres

L’interface **ID3DX10SkinInfo** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10SkinInfo** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10SkinInfo** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddBoneInfluences**](id3dx10skininfo-addboneinfluences.md)           | Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.<br/>     |
| [**AddBones**](id3dx10skininfo-addbones.md)                             | Allouez de l’espace pour d’autres segments.<br/>                                                                                          |
| [**AddVertices**](id3dx10skininfo-addvertices.md)                       | Allouez de l’espace pour des vertex supplémentaires.<br/>                                                                                 |
| [**ClearBoneInfluences**](id3dx10skininfo-clearboneinfluences.md)       | Désactivez la liste des vertex d’un os qu’elle influence.<br/>                                                                     |
| [**Compact**](id3dx10skininfo-compact.md)                               | Limitez le nombre d’os pouvant influencer un vertex et/ou limitez la quantité d’influence qu’un segment peut avoir sur un sommet.<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | Effectuez des dépassements de logiciels sur un tableau de vertex.<br/>                                                                           |
| [**FindBoneInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | Recherche l’index qui indique où un vertex donné figure dans la liste des vertex influencés d’un segment donné.<br/>                    |
| [**GetBoneInfluence**](id3dx10skininfo-getboneinfluence.md)             | Obtenir le degré d’influence d’un segment donné sur un vertex donné.<br/>                                                       |
| [**GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | Obtient le nombre de vertex qu’un segment donné influence.<br/>                                                                |
| [**GetBoneInfluences**](id3dx10skininfo-getboneinfluences.md)           | Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.<br/> |
| [**GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Obtenir le nombre de vertex qu’un segment peut maximiser.<br/>                                                              |
| [**GetNumBones**](id3dx10skininfo-getnumbones.md)                       | Obtient le nombre d’os dans ID3DX10SkinInfo.<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | Obtient le nombre de vertex dans ID3DX10SkinInfo.<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | Modifiez les segments qui influencent les vertex.<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | Modifiez les vertex qui sont influencés par les segments.<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | Supprimer un segment.<br/>                                                                                                          |
| [**SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md)             | Définit le degré d’influence d’un segment donné sur un sommet donné.<br/>                                                       |



 

## <a name="remarks"></a>Notes

Créez une interface ID3DX10SkinInfo avec [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** ou **D3DX10CreateSkinInfoFVF**.

Le type LPD3DX10SKININFO est défini comme un pointeur vers l’interface **ID3DX10SkinInfo** .


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
