---
description: Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex. L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh :: UpdateSemantics, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043117"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>ID3DXBaseMesh :: UpdateSemantics, méthode

Cette méthode permet à l’utilisateur de modifier la déclaration de maillage sans modifier la disposition des données de la mémoire tampon de vertex. L’appel est valide uniquement si l’ancien et le nouveau format de déclaration ont la même taille de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Déclaration* \[ de in, out\]
</dt> <dd>

Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex des vertex de maillage. La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

[**ID3DXBaseMesh :: CloneMesh**](id3dxbasemesh--clonemesh.md) est utilisé pour reformater et modifier la disposition des données de vertex. Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les pondérations, etc. qui n’étaient pas déjà présentes.

**ID3DXBaseMesh :: UpdateSemantics** est une méthode permettant de mettre à jour la déclaration de vertex avec des informations sémantiques différentes, sans modifier la disposition de la mémoire tampon de vertex. Par exemple, utilisez-le pour réétiqueter une coordonnée de texture 3D en tant que biperpendiculaire ou tangente, ou vice versa.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
