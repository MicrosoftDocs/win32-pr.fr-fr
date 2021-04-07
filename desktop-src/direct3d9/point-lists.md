---
description: Une liste de points est une collection de vertex qui sont rendus sous forme de points isolés. Votre application peut les utiliser dans des scènes 3D pour des champs en étoile, ou des lignes en pointillés sur la surface d’un polygone.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listes de points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746780"
---
# <a name="point-lists"></a><span data-ttu-id="4c313-104">Listes de points</span><span class="sxs-lookup"><span data-stu-id="4c313-104">Point Lists</span></span>

<span data-ttu-id="4c313-105">Une liste de points est une collection de vertex qui sont rendus sous forme de points isolés.</span><span class="sxs-lookup"><span data-stu-id="4c313-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="4c313-106">Votre application peut les utiliser dans des scènes 3D pour des champs en étoile, ou des lignes en pointillés sur la surface d’un polygone.</span><span class="sxs-lookup"><span data-stu-id="4c313-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="4c313-107">L’illustration suivante représente une liste de points rendue.</span><span class="sxs-lookup"><span data-stu-id="4c313-107">The following illustration depicts a rendered point list.</span></span>

![illustration d’une liste de points](images/pointlst.png)

<span data-ttu-id="4c313-109">Votre application peut appliquer des matériaux et des textures à une liste de points.</span><span class="sxs-lookup"><span data-stu-id="4c313-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="4c313-110">Les couleurs de la texture ou du matériau apparaissent uniquement aux points dessinés, et pas entre les points.</span><span class="sxs-lookup"><span data-stu-id="4c313-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="4c313-111">Le code suivant montre comment créer des vertex pour cette liste de points.</span><span class="sxs-lookup"><span data-stu-id="4c313-111">The following code shows how to create vertices for this point list.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



<span data-ttu-id="4c313-112">L’exemple de code ci-dessous montre comment afficher cette liste de points dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="4c313-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="4c313-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c313-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c313-114">Primitives</span><span class="sxs-lookup"><span data-stu-id="4c313-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
