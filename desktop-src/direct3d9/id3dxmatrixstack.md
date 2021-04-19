---
description: Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interface ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528573"
---
# <a name="id3dxmatrixstack-interface"></a>Interface ID3DXMATRIXStack

Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.

## <a name="members"></a>Membres

L’interface **ID3DXMATRIXStack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXMATRIXStack** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXMATRIXStack** possède ces méthodes.



| Méthode                                                                       | Description                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Récupère la matrice actuelle en haut de la pile.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack--loadidentity.md)                       | Charge l’identité dans la matrice actuelle.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack--loadmatrix.md)                           | Charge la matrice donnée dans la matrice actuelle.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | Détermine le produit de la matrice actuelle et de la matrice donnée.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | Détermine le produit de la matrice donnée et de la matrice actuelle.<br/>                                                              |
| [**Roulant**](id3dxmatrixstack--pop.md)                                         | Supprime la matrice actuelle du haut de la pile.<br/>                                                                           |
| [**Souleve**](id3dxmatrixstack--push.md)                                       | Ajoute une matrice à la pile.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.<br/>                                             |
| [**Scale**](id3dxmatrixstack--scale.md)                                     | Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.<br/>                                                                               |
| [**Traduire**](id3dxmatrixstack--translate.md)                             | Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.<br/> |



 

## <a name="remarks"></a>Notes

L’interface **ID3DXMATRIXStack** est obtenue en appelant la fonction [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .

Le type LPD3DXMATRIXSTACK est défini comme un pointeur vers l’interface **ID3DXMATRIXStack** .


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
