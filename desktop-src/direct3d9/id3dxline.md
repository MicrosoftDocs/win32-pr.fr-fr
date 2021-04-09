---
description: L’interface ID3DXLine implémente le dessin de lignes à l’aide de triangles texturés.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interface ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043194"
---
# <a name="id3dxline-interface"></a>Interface ID3DXLine

L’interface ID3DXLine implémente le dessin de lignes à l’aide de triangles texturés.

## <a name="members"></a>Membres

L’interface **ID3DXLine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXLine** possède ces méthodes.



| Méthode                                                | Description                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Début**](id3dxline--begin.md)                     | Prépare un appareil pour le dessin de lignes.<br/>                                                                                                                                                  |
| [**Dessin**](id3dxline--draw.md)                       | Dessine une bande en courbes dans l’espace à l’écran. L’entrée se présente sous la forme d’un tableau qui définit les points (of [**D3DXVECTOR2**](d3dxvector2.md)) sur la bande.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Dessine une bande de courbes dans l’espace à l’écran avec une matrice de transformation d’entrée spécifiée.<br/>                                                                                                      |
| [**Effet**](id3dxline--end.md)                         | Restaure l’état de l’appareil sur la manière dont il se trouvait lors de l’appel de [**ID3DXLine :: Begin**](id3dxline--begin.md) .<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Obtient l’état de l’anticrénelage de ligne.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Récupère le périphérique Direct3D associé à l’objet Line.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Obtient le mode de dessin de lignes de style OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Obtient le modèle de stipple de la ligne.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Obtient la valeur de mise à l’échelle du modèle stipple.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Obtient l’épaisseur de la ligne.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Active ou désactive l’anticrénelage de ligne.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Active/désactive le mode de dessin des lignes de style OpenGL.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Applique un modèle de stipple à la ligne.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Étire le modèle stipple le long de la direction de la ligne.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Spécifie l’épaisseur de la ligne.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Notes

Créez un objet de dessin de ligne avec [**D3DXCreateLine**](d3dxcreateline.md).

Le type LPD3DXLINE est défini comme un pointeur vers l’interface **ID3DXLine** .


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
