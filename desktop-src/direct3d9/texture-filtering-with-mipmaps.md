---
description: Un mipmap est une séquence de textures, chacune d’elles étant une représentation de résolution progressivement inférieure de la même image.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtrage de texture avec des mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552236"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtrage de texture avec des mipmaps (Direct3D 9)

Un mipmap est une séquence de textures, chacune d’elles étant une représentation de résolution progressivement inférieure de la même image. La hauteur et la largeur de chaque image, ou niveau, dans le mipmap sont une puissance de deux plus petite que le niveau précédent. Les des mipmaps n’ont pas besoin d’être carrés.

Une image mipmap haute résolution est utilisée pour les objets qui sont proches de l’utilisateur. Les images de résolution inférieure sont utilisées lorsque l’objet apparaît plus loin. Mappage MIP améliore la qualité des textures rendues au détriment de l’utilisation de davantage de mémoire.

Direct3D représente des mipmaps sous la forme d’une chaîne de surfaces attachées. La texture de résolution la plus élevée se trouve au début de la chaîne et a le niveau suivant du mipmap en tant que pièce jointe. À son tour, ce niveau a une pièce jointe qui est le niveau suivant dans le mipmap, et ainsi de suite, jusqu’au niveau de résolution le plus bas du mipmap.

Les illustrations suivantes présentent un exemple de ces niveaux. Les textures de la bitmap représentent un signe sur un conteneur dans un jeu 3D de première personne. En cas de création en tant que mipmap, la texture de résolution la plus élevée est d’abord dans le jeu. Chaque texture qui suit dans l’ensemble de mipmap est plus petite de hauteur et de largeur par une puissance de 2. Dans ce cas, le mipmap à résolution maximale est de 256 pixels par 256 pixels. La texture suivante est 128 x 128. La dernière texture de la chaîne est 64x64.

Ce signe a une distance maximale à partir de laquelle il est visible. Si l’utilisateur commence loin du signe, le jeu affiche la texture la plus petite dans la chaîne mipmap, qui, dans ce cas, la texture 64x64.

![illustration d’une texture 64x64 d’un signe de danger](images/mip1.jpg)

À mesure que l’utilisateur déplace le point de vue plus près du signe, les textures de résolution plus élevée dans la chaîne mipmap sont utilisées. La résolution de l’illustration suivante est 128 x 128.

![illustration d’une texture 128 x 128 d’un signe de danger](images/mip2.jpg)

La texture de résolution la plus élevée est utilisée lorsque le point de vue de l’utilisateur est à la distance minimale autorisée par rapport au signe, comme indiqué dans l’illustration suivante.

![illustration d’une texture 256x256 d’un signe de danger](images/mip3.jpg)

Il s’agit d’un moyen plus efficace de simuler la perspective des textures. Au lieu d’afficher une seule texture à de nombreuses résolutions, il est plus rapide d’utiliser plusieurs textures à des résolutions différentes.

Direct3D peut évaluer quelle texture dans un ensemble de mipmap est la résolution la plus proche de la sortie souhaitée, et elle peut mapper les pixels dans son espace Texel. Si la résolution de l’image finale est comprise entre les résolutions des textures de l’ensemble de mipmap, Direct3D peut examiner les texels dans des mipmaps et fusionner leurs valeurs de couleur ensemble.

Pour utiliser des mipmaps, votre application doit générer un ensemble de des mipmaps. Les applications appliquent des mipmaps en sélectionnant le mipmap défini comme première texture dans le jeu de textures actuelles. Pour plus d’informations, consultez [Blending texture (Direct3D 9)](texture-blending.md).

Ensuite, votre application doit définir la méthode de filtrage utilisée par Direct3D pour échantillonner les texels. La méthode la plus rapide de filtrage mipmap est d’avoir Direct3D Select the Texel le plus proche. Utilisez la \_ valeur d’énumération de point D3DTEXF pour la sélectionner. Direct3D peut produire de meilleurs résultats de filtrage si votre application utilise la \_ valeur énumérée linéaire D3DTEXF. Cela sélectionne le mipmap le plus proche, puis calcule une moyenne pondérée des texels entourant l’emplacement de la texture vers laquelle le pixel actuel est mappé.

Les textures mipmap sont utilisées dans les scènes 3D pour réduire le temps nécessaire au rendu d’une scène. Ils améliorent également le réalisme de la scène. Toutefois, elles nécessitent souvent de grandes quantités de mémoire.

## <a name="creating-a-set-of-mipmaps"></a>Création d’un ensemble de des mipmaps

L’exemple suivant montre comment votre application peut appeler la méthode [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) pour générer une chaîne de cinq niveaux de mipmap : 256x256, 128 x 128, 64x64, 32x32 et 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Les deux premiers paramètres acceptés par [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) sont la taille et la largeur de la texture de niveau supérieur. Le troisième paramètre spécifie le nombre de niveaux dans la texture. Si vous définissez cette valeur sur zéro, Direct3D crée une chaîne de surfaces, chacune d’une puissance de deux plus petite que la précédente, jusqu’à la plus petite taille possible de 1x1. Le quatrième paramètre spécifie l’utilisation de cette ressource. dans ce cas, 0 est spécifié pour indiquer qu’il n’y a pas d’utilisation spécifique pour la ressource. Le cinquième paramètre spécifie le format de surface pour la texture. Utilisez une valeur du type énuméré [D3DFORMAT](d3dformat.md) pour ce paramètre. Le sixième paramètre spécifie un membre du type énuméré [**D3DPOOL**](./d3dpool.md) indiquant la classe de mémoire dans laquelle placer la ressource créée. À moins que vous n’utilisiez des textures dynamiques, D3DPOOL \_ est recommandé. Le dernier paramètre prend l’adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

> [!Note]  
> Chaque surface dans une chaîne mipmap a des dimensions qui représentent une moitié de la surface précédente dans la chaîne. Si le mipmap de niveau supérieur a des dimensions de 256 x 128, les dimensions du mipmap de deuxième niveau sont 128x64, le troisième niveau est 64x32, et ainsi de suite, jusqu’à 1x1. Vous ne pouvez pas demander un certain nombre de niveaux de mipmap dans des niveaux qui provoqueraient une taille inférieure ou égale à 1 de la largeur ou de la hauteur d’un mipmap dans la chaîne. Dans le cas simple d’une surface mipmap de niveau supérieur 4x2, la valeur maximale autorisée pour Levels est trois. Les dimensions de niveau supérieur sont 4x2, les dimensions de second niveau sont 2x1 et les dimensions du troisième niveau sont 1x1. Une valeur supérieure à 3 dans niveaux produit une valeur fractionnaire dans la hauteur du mipmap de deuxième niveau, et n’est donc pas autorisée.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Sélection et affichage d’un mipmap

Appelez la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/desktop/api) pour définir la texture mipmap définie comme première texture dans la liste des textures actuelles. Pour plus d’informations, consultez [Blending texture (Direct3D 9)](texture-blending.md).

Une fois que votre application a sélectionné l’ensemble de textures mipmap, elle doit assigner des valeurs du type énuméré [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) à l’état de l' \_ échantillonneur D3DSAMP MIPFILTER. Direct3D effectue ensuite automatiquement le filtrage de texture mipmap. L’activation du filtrage de texture mipmap est illustrée dans l’exemple de code suivant.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



Votre application peut également parcourir manuellement une chaîne de surfaces mipmap à l’aide de la méthode [**IDirect3DTexture9 :: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) et en spécifiant le niveau de mipmap à récupérer. L’exemple suivant parcourt une chaîne mipmap des résolutions les plus élevées aux plus basses.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Les applications doivent parcourir manuellement une chaîne mipmap pour charger des données bitmap dans chaque surface de la chaîne. Il s’agit généralement de la seule raison de traverser la chaîne. Une application peut récupérer le nombre de niveaux dans un mipmap en appelant [**IDirect3DBaseTexture9 :: GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage de texture](texture-filtering.md)
</dt> </dl>

 

 
