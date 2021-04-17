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
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="ec2ac-103">Ressources de texture de volume (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec2ac-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="ec2ac-104">Les textures de volume sont des collections à trois dimensions de pixels (texels) qui peuvent être utilisées pour peindre une primitive à deux dimensions, telle qu’un triangle ou une ligne.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="ec2ac-105">Des coordonnées de texture à trois éléments sont requises pour chaque vertex d’une primitive qui doit être texturée avec un volume.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="ec2ac-106">Lorsque la primitive est dessinée, chaque pixel contenu est rempli avec la valeur de couleur d’un pixel du volume, conformément aux règles analogues au cas de texture à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="ec2ac-107">Les volumes ne sont pas restitués directement, car il n’existe pas de primitives tridimensionnelles qui peuvent être peintes avec eux.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="ec2ac-108">Vous pouvez utiliser des textures de volume pour des effets spéciaux, tels que le brouillard correctif, les explosions, etc.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="ec2ac-109">Les volumes sont organisés en tranches et peuvent être considérés comme des surfaces 2D de largeur x hauteur empilées pour créer un volume de profondeur x hauteur x profondeur.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="ec2ac-110">Chaque tranche est une ligne unique.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-110">Each slice is a single row.</span></span> <span data-ttu-id="ec2ac-111">Les volumes peuvent avoir des niveaux suivants, dans lesquels les dimensions de chaque niveau sont tronquées à la moitié des dimensions du niveau précédent.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="ec2ac-112">Le diagramme suivant montre à quoi ressemble une texture de volume à plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![diagramme d’une texture de volume avec des représentations de cube 8x2x4, 4x1x2 et 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="ec2ac-114">Création d’une texture de volume</span><span class="sxs-lookup"><span data-stu-id="ec2ac-114">Creating a Volume Texture</span></span>

<span data-ttu-id="ec2ac-115">Les exemples de code ci-dessous illustrent les étapes nécessaires à l’utilisation d’une texture de volume.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="ec2ac-116">Tout d’abord, spécifiez un type de vertex personnalisé qui a trois coordonnées de texture pour chaque vertex, comme indiqué dans cet exemple de code.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


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



<span data-ttu-id="ec2ac-117">Ensuite, remplissez les vertex avec des données.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="ec2ac-118">À présent, créez une mémoire tampon de vertex et remplissez-la avec les données des vertex.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="ec2ac-119">L’étape suivante consiste à utiliser la méthode [**IDirect3DDevice9 :: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) pour créer une texture de volume, comme indiqué dans cet exemple de code.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="ec2ac-120">Avant de rendre la primitive, définissez la texture actuelle sur la texture de volume créée ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="ec2ac-121">L’exemple de code ci-dessous montre l’intégralité du processus de rendu pour une bande de triangles.</span><span class="sxs-lookup"><span data-stu-id="ec2ac-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ec2ac-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec2ac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec2ac-123">Textures Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec2ac-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
