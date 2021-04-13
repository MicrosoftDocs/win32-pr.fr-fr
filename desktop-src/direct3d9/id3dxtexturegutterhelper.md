---
description: L’interface ID3DXTextureGutterHelper est utilisée pour créer et gérer des zones de marge dans une texture. Les régions de reliure séparent les textures et permettent l’interpolation bilinéaire afin d’éviter le rendu des artefacts aux limites de la texture.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interface ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323222"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Interface ID3DXTextureGutterHelper

L’interface ID3DXTextureGutterHelper est utilisée pour créer et gérer des zones de marge dans une texture. Les régions de reliure séparent les textures et permettent l’interpolation bilinéaire afin d’éviter le rendu des artefacts aux limites de la texture.

Le... les méthodes fournissent l’accès aux structures de données utilisées par l’application... leurs.

## <a name="members"></a>Membres

L’interface **ID3DXTextureGutterHelper** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureGutterHelper** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXTextureGutterHelper** possède ces méthodes.



| Méthode                                                                   | Description                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Applique des reliures à une mémoire tampon de texture FLOTTante.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Applique des gouttières à un objet de mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Applique des gouttières à un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Récupère les coordonnées Barycentric texels.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Récupère l’index du type de maillage auquel appartient chaque Texel.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Reçoit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Récupère la hauteur de la texture, en pixels.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Récupère les coordonnées de texture (u, v) de chaque Texel.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Récupère la largeur de la texture, en pixels.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Rééchantillonne une texture dans le paramétrage de ce gutterhelper.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Définit les coordonnées Barycentric texels.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Définit l’index du type de maillage auquel appartient chaque Texel.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Définit une valeur de classe Texel qui indique la classe Texel en fonction de l’emplacement de chaque Texel.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Définit les coordonnées de texture (u, v) de chaque Texel.<br/>                                          |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Lorsqu’elle est utilisée avec le luminance de transfert précalculé (PRT), cette interface requiert un paramétrage unique du modèle. Chaque Texel doit correspondre à un point unique sur la surface du modèle et vice versa. Si le modèle comprend plusieurs textures, celles-ci doivent être fractionnées en éléments distincts qui contiennent chacun un objet d’assistance de gouttière par texture.

 

Cette interface peut être utilisée pour générer un mappage dans l’espace de texture dans lequel chaque Texel est dans l’une des quatre classes.



| Texel (classe) | Emplacement de Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Point non valide ; Texel ne sera pas utilisé.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triangle intérieur.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Marge intérieure.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Marge intérieure ; Texel sera évalué comme un exemple complet dans les méthodes [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper :: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper :: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

Pour les classes 1 et 2, un Texel est stocké avec la face à laquelle il appartient, ainsi que les coordonnées Barycentric des deux premiers sommets de ce visage. Les sommets de la reliure sont affectés au bord le plus proche dans l’espace de texture.

Il n’existe pas de classe Texel 3.

L’interface **ID3DXTextureGutterHelper** est obtenue en appelant la fonction [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .

Le type LPD3DXTEXTUREGUTTERHELPER est défini comme un pointeur vers l’interface **ID3DXTextureGutterHelper** .


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
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

 

 
