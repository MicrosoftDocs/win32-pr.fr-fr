---
description: Une bande triangulaire est une série de triangles connectés.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Bandes triangulaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557769"
---
# <a name="triangle-strips"></a><span data-ttu-id="b2796-103">Bandes triangulaires</span><span class="sxs-lookup"><span data-stu-id="b2796-103">Triangle Strips</span></span>

<span data-ttu-id="b2796-104">Une bande triangulaire est une série de triangles connectés.</span><span class="sxs-lookup"><span data-stu-id="b2796-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="b2796-105">Étant donné que les triangles sont connectés, l’application n’a pas besoin de spécifier à plusieurs reprises les trois vertex pour chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="b2796-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="b2796-106">Par exemple, vous n’avez besoin que de sept sommets pour définir la bande triangulaire suivante.</span><span class="sxs-lookup"><span data-stu-id="b2796-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![illustration d’une bande triangulaire avec sept sommets](images/tristrip.png)

<span data-ttu-id="b2796-108">Le système utilise les vertex v1, v2 et v3 pour dessiner le premier triangle. v2, V4 et v3 pour dessiner le deuxième triangle ; v3, V4 et V5 pour dessiner le troisième ; v4, V6 et V5 pour dessiner le quatrième ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b2796-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="b2796-109">Notez que les sommets du deuxième et du quatrième triangles sont dans le désordre. Cela est nécessaire pour s’assurer que tous les triangles sont dessinés dans l’orientation dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="b2796-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="b2796-110">La plupart des objets dans les scènes 3D sont composés de bandes triangulaires.</span><span class="sxs-lookup"><span data-stu-id="b2796-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="b2796-111">Cela est dû au fait que les bandes de triangle peuvent être utilisées pour spécifier des objets complexes d’une manière qui utilise efficacement la mémoire et le temps de traitement.</span><span class="sxs-lookup"><span data-stu-id="b2796-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="b2796-112">L’illustration suivante représente une bande triangulaire rendue.</span><span class="sxs-lookup"><span data-stu-id="b2796-112">The following illustration depicts a rendered triangle strip.</span></span>

![illustration d’une bande triangulaire rendue](images/tstrip2.png)

<span data-ttu-id="b2796-114">Le code suivant montre comment créer des vertex pour cette bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="b2796-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="b2796-115">L’exemple de code ci-dessous montre comment restituer cette bande triangulaire dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="b2796-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="b2796-116">Utilisez une bande triangulaire pour restituer des triangles qui ne sont pas connectés les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="b2796-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="b2796-117">Pour ce faire, spécifiez un triangle dégenerate (autrement dit, un triangle dont la zone est égale à zéro) dans la liste de triangles.</span><span class="sxs-lookup"><span data-stu-id="b2796-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="b2796-118">Cela crée une ligne entre les deux triangles qui ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="b2796-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="b2796-119">Pour afficher uniquement le premier et le dernier triangles de l’exemple précédent, modifiez la mémoire tampon du vertex comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="b2796-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b2796-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2796-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2796-121">Primitives</span><span class="sxs-lookup"><span data-stu-id="b2796-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
