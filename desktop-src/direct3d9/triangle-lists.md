---
description: Une liste triangulaire est une liste de triangles isolés. Ils peuvent être ou ne pas se rapprocher les uns des autres. Une liste de triangles doit avoir au moins trois vertex et le nombre total de vertex doit être divisible par trois.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listes de triangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513908"
---
# <a name="triangle-lists"></a><span data-ttu-id="c707e-105">Listes de triangles</span><span class="sxs-lookup"><span data-stu-id="c707e-105">Triangle Lists</span></span>

<span data-ttu-id="c707e-106">Une liste triangulaire est une liste de triangles isolés.</span><span class="sxs-lookup"><span data-stu-id="c707e-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="c707e-107">Ils peuvent être ou ne pas se rapprocher les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="c707e-107">They might or might not be near each other.</span></span> <span data-ttu-id="c707e-108">Une liste de triangles doit avoir au moins trois vertex et le nombre total de vertex doit être divisible par trois.</span><span class="sxs-lookup"><span data-stu-id="c707e-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="c707e-109">Utilisez des listes de triangles pour créer un objet composé de pièces disjointes.</span><span class="sxs-lookup"><span data-stu-id="c707e-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="c707e-110">Par exemple, une façon de créer un mur de champ de force dans un jeu 3D consiste à spécifier une grande liste de petits triangles non connectés.</span><span class="sxs-lookup"><span data-stu-id="c707e-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="c707e-111">Appliquez ensuite un matériau et une texture qui semblent émettre de la lumière dans la liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="c707e-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="c707e-112">Chaque triangle du mur semble briller.</span><span class="sxs-lookup"><span data-stu-id="c707e-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="c707e-113">La scène derrière le mur devient partiellement visible à travers les intervalles entre les triangles, car un joueur peut s’attendre à voir un champ force.</span><span class="sxs-lookup"><span data-stu-id="c707e-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="c707e-114">Les listes de triangles sont également utiles pour créer des primitives qui ont des bords tranchants et qui sont ombrées avec l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="c707e-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="c707e-115">Consultez [vecteurs normaux de face et vertex (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="c707e-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="c707e-116">L’illustration suivante représente une liste de triangles rendue.</span><span class="sxs-lookup"><span data-stu-id="c707e-116">The following illustration depicts a rendered triangle list.</span></span>

![illustration d’une liste de triangles rendue](images/trilist.png)

<span data-ttu-id="c707e-118">Le code suivant montre comment créer des vertex pour cette liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="c707e-118">The following code shows how to create vertices for this triangle list.</span></span>


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



<span data-ttu-id="c707e-119">L’exemple de code ci-dessous montre comment afficher cette liste de triangles dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="c707e-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="c707e-120">Vous pouvez également utiliser des bandes triangulaires pour afficher des triangles qui ne sont pas connectés les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="c707e-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="c707e-121">Pour ce faire, spécifiez un triangle dégenerate (autrement dit, un triangle avec une taille nulle) dans la liste ; Cette opération crée une ligne entre les deux triangles qui n’apparaît pas pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="c707e-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="c707e-122">Par exemple, pour afficher uniquement le premier et le dernier triangle de l’exemple précédent, initialisez la mémoire tampon de vertex avec les vertex suivants :</span><span class="sxs-lookup"><span data-stu-id="c707e-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="c707e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c707e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c707e-124">Primitives</span><span class="sxs-lookup"><span data-stu-id="c707e-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
