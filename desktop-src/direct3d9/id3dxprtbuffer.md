---
description: L’interface ID3DXPRTBuffer est utilisée comme mémoire tampon de données pour stocker les données de vertex et de pixels à utiliser avec les méthodes et les fonctions de transfert luminance (PRT) précalculées.
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interface ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522999"
---
# <a name="id3dxprtbuffer-interface"></a>Interface ID3DXPRTBuffer

L’interface ID3DXPRTBuffer est utilisée comme mémoire tampon de données pour stocker les données de vertex et de pixels à utiliser avec les méthodes et les fonctions de transfert luminance (PRT) précalculées.

## <a name="members"></a>Membres

L’interface **ID3DXPRTBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXPRTBuffer** possède ces méthodes.



| Méthode                                                   | Description                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Ajoute une autre mémoire tampon au **ID3DXPRTBuffer** et stocke les résultats dans **ID3DXPRTBuffer**.<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Associe un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à l’objet **ID3DXPRTBuffer** .<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Applique les données de marge de texture stockées à une mémoire tampon de texture **ID3DXPRTBuffer** .<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .<br/>                                                              |
| [**GetHeight**](id3dxprtbuffer--getheight.md)           | Récupère la hauteur de la texture, en pixels.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Récupère le nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Récupère le nombre de vertex (ou de texels) échantillonnés.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Récupère la largeur de la texture, en pixels.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Indique si la mémoire tampon contient une texture.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Dissocie un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) joint avec l’objet **ID3DXPRTBuffer** .<br/>                                                   |
| [**Redimensionner**](id3dxprtbuffer--resize.md)                 | Modifie le nombre d’échantillons contenus dans la mémoire tampon.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Multiplie chaque valeur de la mémoire tampon par une valeur de constante.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Termine la durée de vie du pointeur ppData retourné par [**ID3DXPRTBuffer :: LockBuffer**](id3dxprtbuffer--lockbuffer.md).<br/>                                                              |



 

## <a name="remarks"></a>Notes

L’interface **ID3DXPRTBuffer** est obtenue en appelant les fonctions [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .

Le type LPD3DXPRTBUFFER est défini comme un pointeur vers l’interface **ID3DXPRTBuffer** .


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
