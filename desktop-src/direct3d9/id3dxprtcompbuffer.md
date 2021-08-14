---
description: L’interface ID3DXPRTCompBuffer stocke une version compressée d’une mémoire tampon ID3DXPRTBuffer, à utiliser avec l’analyse des composants principaux (PCA, principal Component Analysis).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interface ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a84f1bc7b25af0c900f5587ba0d1dd948cac39bc52f706ff389c0ca9d053ec0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985609"
---
# <a name="id3dxprtcompbuffer-interface"></a>Interface ID3DXPRTCompBuffer

L’interface **ID3DXPRTCompBuffer** stocke une version compressée d’une mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , à utiliser avec l’analyse des composants principaux (PCA, principal Component Analysis).

## <a name="members"></a>Membres

L’interface **ID3DXPRTCompBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTCompBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXPRTCompBuffer** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | Extrait les vecteurs de base de la moyenne et de l’analyse des composants principaux (PCA) pour un cluster donné à partir d’une mémoire tampon de données compressées **ID3DXPRTCompBuffer** .<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | Extrait les ID de cluster par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** .<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** .<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | Récupère la hauteur de la texture, en pixels.<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | Récupère le nombre de clusters à utiliser pour la compression.<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Récupère le nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples.<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | Récupère le nombre de vecteurs de base de l’analyse des composants principaux (PCA) à utiliser dans chaque cluster.<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | Récupère le nombre de vertex (ou de texels) échantillonnés.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Récupère la largeur de la texture, en pixels.<br/>                                                                                                                                                                          |
| [**IsTexture**](id3dxprtcompbuffer--istexture.md)                 | Indique si la mémoire tampon contient une texture.<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1. Les vecteurs de base sont modifiés pour refléter cette normalisation.<br/>                                                                  |



 

## <a name="remarks"></a>Remarques

L’interface **ID3DXPRTCompBuffer** est obtenue en appelant la fonction [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .

Le type LPD3DXPRTCOMPBUFFER est défini comme un pointeur vers l’interface **ID3DXPRTCompBuffer** .


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
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

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
