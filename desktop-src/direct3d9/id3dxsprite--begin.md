---
description: Prépare un appareil pour le dessin des sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite :: Begin, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94d3ee659937508f52e38513006701494a01ed4ff95fe6c75c56bd9638137160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277829"
---
# <a name="id3dxspritebegin-method"></a>ID3DXSprite :: Begin, méthode

Prépare un appareil pour le dessin des sprites.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de zéro, un ou plusieurs indicateurs qui décrivent les options de rendu Sprite. Pour cette méthode, les indicateurs valides sont les suivants :

-   D3DXSPRITE \_ ALPHABLEND
-   \_ \_ Panneau D3DXSPRITE
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTSPACE
-   D3DXSPRITE \_ \_ profondeur de tri \_ \_ BACKTOFRONT
-   D3DXSPRITE \_ \_ profondeur de tri \_ \_ FRONTTOBACK
-   \_ \_ Texture de tri D3DXSPRITE \_

Pour obtenir une description des indicateurs et pour plus d’informations sur la façon de contrôler la capture de l’état des appareils et des transformations d’affichage des appareils, consultez [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette méthode doit être appelée à partir d’un [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) . . . Séquence [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) . **ID3DXSprite :: Begin** ne peut pas être utilisé comme substitut pour **IDirect3DDevice9 :: BeginScene** ou [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md).

Cette méthode définit les États suivants sur l’appareil.

États de rendu :



| Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Valeur                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | TRUE                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ plus                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ Ajouter                                                                                                   |
| \_Découpage D3DRS                                               | TRUE                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ alpha \| D3DCOLORWRITEENABLE \_ bleu \| D3DCOLORWRITEENABLE \_ vert \| D3DCOLORWRITEENABLE \_ rouge |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ aucun                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FillMode                                               | D3DFILL \_ Solid                                                                                                    |
| D3DRS \_ FOGENABLE                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| \_Éclairage D3DRS                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ Gouraud                                                                                                 |
| D3DRS \_ SpecularEnable                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

États des étapes de texture :



| Identificateur de l’étape | Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Valeur            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | \_Texture D3DTA   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | \_Diffusion D3DTA   |
| 0                | D3DTSS \_ ALPHAOP                                                           | \_Modulation D3DTOP |
| 0                | D3DTSS \_ COLORARG1                                                         | \_Texture D3DTA   |
| 0                | D3DTSS \_ COLORARG2                                                         | \_Diffusion D3DTA   |
| 0                | D3DTSS \_ COLOROP                                                           | \_Modulation D3DTOP |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | Désactivation de D3DTTFF \_ |
| 1                | D3DTSS \_ ALPHAOP                                                           | Désactivation de D3DTOP \_  |
| 1                | D3DTSS \_ COLOROP                                                           | Désactivation de D3DTOP \_  |



 

États de l’échantillonneur :



| Index d’étape de l’échantillonneur | Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Valeur                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | \_Adresse D3DSAMP                                               | D3DTADDRESS \_ clamp                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS \_ clamp                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ anisotrope si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MAGFANISOTROPIC ; sinon, D3DTEXF \_ linéaire |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ anisotrope si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MINFANISOTROPIC ; sinon, D3DTEXF \_ linéaire |
| 0                   | D3DSAMP \_ MIPFILTER                                              | D3DTEXF \_ Linear si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MIPFLINEAR ; sinon D3DTEXF \_ point            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Cette méthode désactive N-patchs.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
