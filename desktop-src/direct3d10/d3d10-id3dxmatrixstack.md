---
description: 'Interface ID3DXMatrixStack : les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.'
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interface ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094407"
---
# <a name="id3dxmatrixstack-interface"></a>Interface ID3DXMatrixStack

Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.

## <a name="members"></a>Membres

L’interface **ID3DXMatrixStack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXMatrixStack** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXMatrixStack** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Récupère la matrice actuelle en haut de la pile.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack-loadidentity.md)                       | Charge l’identité dans la matrice actuelle.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack-loadmatrix.md)                           | Charge la matrice donnée dans la matrice actuelle.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack-multmatrix.md)                           | Détermine le produit de la matrice actuelle et de la matrice donnée.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Détermine le produit de la matrice donnée et de la matrice actuelle.<br/>                                                              |
| [**Roulant**](id3dxmatrixstack-pop.md)                                         | Supprime la matrice actuelle du haut de la pile.<br/>                                                                           |
| [**Souleve**](id3dxmatrixstack-push.md)                                       | Ajoute une matrice à la pile.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack-rotateaxis.md)                           | Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Pivote (par rapport à l’espace de coordonnées universelles) autour d’un axe arbitraire.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.<br/>                                             |
| [**Scale**](id3dxmatrixstack-scale.md)                                     | Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack-scalelocal.md)                           | Mettre à l’échelle la matrice actuelle sur l’origine de l’objet.<br/>                                                                               |
| [**Translate**](id3dxmatrixstack-translate.md)                             | Détermine le produit de la matrice actuelle et la matrice de translation calculée déterminée par les facteurs donnés (x, y et z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack-translatelocal.md)                   | Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.<br/> |



 

## <a name="remarks"></a>Notes 

L’interface ID3DX10MATRIXStack est obtenue en appelant la fonction [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .

Le type LPD3DX10MATRIXSTACK est défini comme un pointeur vers l’interface **ID3DXMatrixStack** .


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
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

 

 
