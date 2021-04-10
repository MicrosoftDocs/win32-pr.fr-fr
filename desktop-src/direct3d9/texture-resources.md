---
description: 'Les ressources de texture sont implémentées dans l’interface IDirect3DTexture9. Pour obtenir un pointeur vers une interface de texture, appelez la méthode IDirect3DDevice9 :: CreateTexture ou l’une des fonctions D3DX suivantes.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Ressources de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200813"
---
# <a name="texture-resources-direct3d-9"></a>Ressources de texture (Direct3D 9)

Les ressources de texture sont implémentées dans l’interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) . Pour obtenir un pointeur vers une interface de texture, appelez la méthode [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ou l’une des fonctions D3DX suivantes.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

L’exemple de code suivant utilise [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) pour charger une texture à partir de Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Le premier paramètre que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepte est un pointeur vers une interface [**IDirect3DDevice9**](/windows/desktop/api) . Le deuxième paramètre indique à Direct3D le nom du fichier à partir duquel la texture doit être chargée. Le troisième paramètre prend l’adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , représentant l’objet de texture créé.

## <a name="rendering-with-texture-resources"></a>Rendu avec des ressources de texture

Direct3D prend en charge la fusion de plusieurs textures par le biais du concept de étapes de texture. Chaque étape de texture contient une texture et des opérations qui peuvent être effectuées sur la texture. Les textures dans les étapes de texture forment le jeu de textures actuelles. Pour plus d’informations, consultez [Blending texture (Direct3D 9)](texture-blending.md). L’état de chaque texture est encapsulé dans son étape de texture.

Dans une application C++, l’état de chaque texture doit être défini à l’aide de la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api) . Transmettez le numéro intermédiaire (0-7) en tant que valeur du premier paramètre. Définissez la valeur du deuxième paramètre sur un membre du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Le dernier paramètre est la valeur d’État pour l’état de texture particulier.

À l’aide de pointeurs d’interface de texture, votre application peut restituer une fusion allant jusqu’à huit textures. Définissez les textures actuelles en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Direct3D fusionne toutes les textures actuelles sur les primitives qu’elle restitue.

> [!Note]  
> La méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrémente le décompte de références de la surface de texture qui est assignée. Lorsque la texture n’est plus nécessaire, vous devez définir la texture à l’étape appropriée sur **null**. Si vous ne le faites pas, la surface n’est pas libérée, ce qui entraîne une fuite de mémoire.

 

Votre application peut définir l’état d’habillage de texture pour les textures actuelles en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . Transmettez une valeur de D3DRS \_ WRAP0 à D3DRS \_ WRAP7 comme valeur du premier paramètre et utilisez une combinaison des \_ indicateurs D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 et D3DWRAPCOORD \_ 3 pour activer l’habillage dans les directions u, v ou w.

Votre application peut également définir la perspective de texture et les États de filtrage de texture. Consultez [filtrage de texture (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
