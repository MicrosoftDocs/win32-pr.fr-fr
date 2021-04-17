---
description: Les textures de volume sont des collections à trois dimensions de pixels (texels) qui peuvent être utilisées pour peindre une primitive à deux dimensions, telle qu’un triangle ou une ligne.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Ressources de texture de volume (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104565087"
---
# <a name="volume-texture-resources-direct3d-9"></a>Ressources de texture de volume (Direct3D 9)

Les textures de volume sont des collections à trois dimensions de pixels (texels) qui peuvent être utilisées pour peindre une primitive à deux dimensions, telle qu’un triangle ou une ligne. Des coordonnées de texture à trois éléments sont requises pour chaque vertex d’une primitive qui doit être texturée avec un volume. Lorsque la primitive est dessinée, chaque pixel contenu est rempli avec la valeur de couleur d’un pixel du volume, conformément aux règles analogues au cas de texture à deux dimensions. Les volumes ne sont pas restitués directement, car il n’existe pas de primitives tridimensionnelles qui peuvent être peintes avec eux.

Vous pouvez utiliser des textures de volume pour des effets spéciaux, tels que le brouillard correctif, les explosions, etc.

Les volumes sont organisés en tranches et peuvent être considérés comme des surfaces 2D de largeur x hauteur empilées pour créer un volume de profondeur x hauteur x profondeur. Chaque tranche est une ligne unique. Les volumes peuvent avoir des niveaux suivants, dans lesquels les dimensions de chaque niveau sont tronquées à la moitié des dimensions du niveau précédent. Le diagramme suivant montre à quoi ressemble une texture de volume à plusieurs niveaux.

![diagramme d’une texture de volume avec des représentations de cube 8x2x4, 4x1x2 et 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Création d’une texture de volume

Les exemples de code ci-dessous illustrent les étapes nécessaires à l’utilisation d’une texture de volume.

Tout d’abord, spécifiez un type de vertex personnalisé qui a trois coordonnées de texture pour chaque vertex, comme indiqué dans cet exemple de code.


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



Ensuite, remplissez les vertex avec des données.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



À présent, créez une mémoire tampon de vertex et remplissez-la avec les données des vertex.

L’étape suivante consiste à utiliser la méthode [**IDirect3DDevice9 :: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) pour créer une texture de volume, comme indiqué dans cet exemple de code.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Avant de rendre la primitive, définissez la texture actuelle sur la texture de volume créée ci-dessus. L’exemple de code ci-dessous montre l’intégralité du processus de rendu pour une bande de triangles.


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
