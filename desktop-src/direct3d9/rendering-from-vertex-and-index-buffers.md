---
description: Direct3D prend en charge les méthodes de dessin indexées et non indexées.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845961"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="908cc-103">Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="908cc-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="908cc-104">Direct3D prend en charge les méthodes de dessin indexées et non indexées.</span><span class="sxs-lookup"><span data-stu-id="908cc-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="908cc-105">Les méthodes indexées utilisent un ensemble unique d’index pour tous les composants de vertex.</span><span class="sxs-lookup"><span data-stu-id="908cc-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="908cc-106">Les données de vertex sont stockées dans des mémoires tampons de vertex, et les données d’index sont stockées dans des mémoires tampons d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="908cc-107">Voici quelques scénarios courants de dessin de primitives utilisant des tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="908cc-108">Ces exemples comparent l’utilisation de [**IDirect3DDevice9 ::D rawprimitive**](/windows/desktop/api) et [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="908cc-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="908cc-109">Scénario 1 : dessin de deux triangles sans indexation</span><span class="sxs-lookup"><span data-stu-id="908cc-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="908cc-110">Supposons que vous souhaitiez dessiner le quadruple qui est représenté dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="908cc-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![illustration d’un carré constitué de deux triangles](images/dip-fig1.png)

<span data-ttu-id="908cc-112">Si vous utilisez le type de primitive List de triangle pour restituer les deux triangles, chaque triangle est stocké sous la forme de 3 Vertex individuels, ce qui donne une mémoire tampon de vertex similaire à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="908cc-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![diagramme d’une mémoire tampon de vertex qui définit trois vertex pour deux triangles](images/dip-fig2.png)

<span data-ttu-id="908cc-114">L’appel de dessin est très simple ; à partir de l’emplacement 0 dans la mémoire tampon de vertex, dessinez deux triangles.</span><span class="sxs-lookup"><span data-stu-id="908cc-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="908cc-115">Si l’élimination est activée, l’ordre des vertex sera important.</span><span class="sxs-lookup"><span data-stu-id="908cc-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="908cc-116">Cet exemple est basé sur l’État par défaut de l’élimination dans le sens inverse des aiguilles d’une montre. les triangles visibles doivent donc être dessinés dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="908cc-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="908cc-117">Le type primitif de liste de triangles lit simplement trois vertex dans l’ordre linéaire à partir de la mémoire tampon pour chaque triangle. cet appel dessinera donc des triangles (0, 1, 2) et (3, 4, 5) :</span><span class="sxs-lookup"><span data-stu-id="908cc-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="908cc-118">Scénario 2 : dessin de deux triangles avec indexation</span><span class="sxs-lookup"><span data-stu-id="908cc-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="908cc-119">Comme vous pouvez le constater, la mémoire tampon de vertex contient des données en double dans les emplacements 0 et 4, 2 et 5.</span><span class="sxs-lookup"><span data-stu-id="908cc-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="908cc-120">Cela est logique, car les deux triangles partagent deux vertex communs.</span><span class="sxs-lookup"><span data-stu-id="908cc-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="908cc-121">Ces données dupliquées sont inutiles et la mémoire tampon de vertex peut être compressée à l’aide d’une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="908cc-122">Une mémoire tampon de vertex plus petite réduit la quantité de données de vertex qui doit être envoyée à la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="908cc-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="908cc-123">Plus important encore, l’utilisation d’un tampon d’index permet à l’adaptateur de stocker des vertex dans un cache de vertex ; Si la primitive qui est dessinée contient un vertex récemment utilisé, ce vertex peut être extrait du cache au lieu de le lire à partir de la mémoire tampon de vertex, ce qui entraîne une augmentation importante des performances.</span><span class="sxs-lookup"><span data-stu-id="908cc-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="908cc-124">Une mémoire tampon d’index « indexe » dans la mémoire tampon de vertex afin que chaque vertex unique doive être stocké une seule fois dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="908cc-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="908cc-125">Le diagramme suivant illustre une approche indexée du scénario de dessin précédent.</span><span class="sxs-lookup"><span data-stu-id="908cc-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![diagramme d’une mémoire tampon d’index pour la mémoire tampon de vertex précédente](images/dip-fig3.png)

<span data-ttu-id="908cc-127">La mémoire tampon d’index stocke les valeurs d’index VB, qui font référence à un vertex particulier dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="908cc-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="908cc-128">Une mémoire tampon de vertex peut être considérée comme un tableau de vertex, donc l’index VB est simplement l’index dans la mémoire tampon de vertex pour le vertex cible.</span><span class="sxs-lookup"><span data-stu-id="908cc-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="908cc-129">De même, un index IB est un index dans le tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="908cc-130">Cela peut s’avérer très confus très rapidement si vous n’êtes pas vigilant. Assurez-vous que vous êtes bien sûr du vocabulaire utilisé : index des valeurs d’index VB dans la mémoire tampon de vertex, index des valeurs d’index IB dans le tampon d’index, et le tampon d’index lui-même stocke les valeurs d’index VB.</span><span class="sxs-lookup"><span data-stu-id="908cc-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="908cc-131">L’appel de dessin est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="908cc-131">The drawing call is shown below.</span></span> <span data-ttu-id="908cc-132">Les significations de tous les arguments sont discutées à la longueur du scénario de dessin suivant. pour le moment, il vous suffit de noter que cet appel demande à Direct3D de restituer une liste de triangles contenant deux triangles, en commençant à l’emplacement 0 dans la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="908cc-133">Cet appel dessinera les deux mêmes triangles dans le même ordre que précédemment, garantissant ainsi une orientation appropriée dans le sens des aiguilles d’une montre :</span><span class="sxs-lookup"><span data-stu-id="908cc-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="908cc-134">Scénario 3 : dessin d’un triangle avec indexation</span><span class="sxs-lookup"><span data-stu-id="908cc-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="908cc-135">Supposons maintenant que vous souhaitez dessiner uniquement le deuxième triangle, mais que vous souhaitez utiliser la même mémoire tampon de vertex et la même mémoire tampon d’index que ceux utilisés lors du dessin de la totalité du quadruple, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="908cc-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![diagramme du tampon d’index et de la mémoire tampon de vertex pour le deuxième triangle](images/dip-fig4.png)

<span data-ttu-id="908cc-137">Pour cet appel de dessin, le premier index IB utilisé est 3 ; Cette valeur est appelée StartIndex.</span><span class="sxs-lookup"><span data-stu-id="908cc-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="908cc-138">L’index VB le plus bas utilisé est 0 ; Cette valeur est appelée MinIndex.</span><span class="sxs-lookup"><span data-stu-id="908cc-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="908cc-139">Même si seuls trois vertex sont requis pour dessiner le triangle, ces trois vertex sont répartis sur quatre emplacements adjacents dans la mémoire tampon de vertex ; le nombre d’emplacements dans le bloc contigu de mémoire tampon de vertex requis pour l’appel de dessin est appelé NumVertices et sera défini sur 4 dans cet appel.</span><span class="sxs-lookup"><span data-stu-id="908cc-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="908cc-140">Les valeurs MinIndex et NumVertices sont en fait simplement des indications pour aider Direct3D à optimiser l’accès à la mémoire lors du traitement des vertex logiciels et peuvent simplement être définies pour inclure l’intégralité de la mémoire tampon du vertex au prix des performances.</span><span class="sxs-lookup"><span data-stu-id="908cc-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="908cc-141">Voici l’appel de dessin pour le cas à triangle unique ; la signification de l’argument BaseVertexIndex sera expliquée ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="908cc-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="908cc-142">Scénario 4 : dessin d’un triangle avec l’indexation de décalage</span><span class="sxs-lookup"><span data-stu-id="908cc-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="908cc-143">BaseVertexIndex est une valeur ajoutée à chaque index VB stocké dans la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="908cc-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="908cc-144">Par exemple, si nous avions passé la valeur 50 pour BaseVertexIndex lors de l’appel précédent, cela équivaut à utiliser le tampon d’index dans le diagramme suivant pour la durée de l’appel DrawIndexedPrimitive :</span><span class="sxs-lookup"><span data-stu-id="908cc-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![diagramme d’une mémoire tampon d’index avec une valeur de 50 pour basevertexindex](images/dip-fig5.png)

<span data-ttu-id="908cc-146">Cette valeur est rarement définie sur une valeur différente de 0, mais peut être utile si vous souhaitez découpler le tampon d’index de la mémoire tampon de vertex : si, lors du remplissage du tampon d’index pour un maillage particulier, l’emplacement du maillage dans la mémoire tampon de vertex n’est pas encore connu, vous pouvez simplement faire en sorte que les sommets du maillage soient situés au début lorsqu’il est temps d’effectuer l’appel de dessin, transmettez simplement l’emplacement de départ réel en tant que BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="908cc-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="908cc-147">Cette technique peut également être utilisée lors du dessin de plusieurs instances d’une maille à l’aide d’une seule mémoire tampon d’index ; par exemple, si la mémoire tampon de vertex contenait deux mailles avec un ordre de dessin identique mais des vertex légèrement différents (peut-être des couleurs diffuses ou des coordonnées de texture différentes), les deux mailles peuvent être dessinées à l’aide de différentes valeurs pour BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="908cc-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="908cc-148">Grâce à ce concept, vous pouvez utiliser une seule mémoire tampon d’index pour dessiner plusieurs instances d’une maille, chacune contenue dans une mémoire tampon de vertex différente, en recourant simplement à la mémoire tampon de vertex active et en ajustant les BaseVertexIndex en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="908cc-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="908cc-149">Notez que la valeur BaseVertexIndex est également ajoutée automatiquement à l’argument MinIndex, ce qui est utile lorsque vous voyez comment il est utilisé :</span><span class="sxs-lookup"><span data-stu-id="908cc-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="908cc-150">Supposons maintenant que nous voulons à nouveau dessiner uniquement le deuxième triangle du Quad en utilisant le même tampon d’index qu’auparavant ; Toutefois, une autre mémoire tampon de vertex est utilisée dans laquelle le quad est situé à l’index VB 50.</span><span class="sxs-lookup"><span data-stu-id="908cc-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="908cc-151">L’ordre relatif des vertex Quad reste inchangé, seul l’emplacement de départ dans la mémoire tampon de vertex est différent.</span><span class="sxs-lookup"><span data-stu-id="908cc-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="908cc-152">Le tampon d’index et la mémoire tampon de vertex ressemblent au diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="908cc-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![diagramme du tampon d’index et de la mémoire tampon de vertex avec un index VB de 50](images/dip-fig6.png)

<span data-ttu-id="908cc-154">Voici l’appel de dessin approprié ; Notez que BaseVertexIndex est la seule valeur qui a changé par rapport au scénario précédent :</span><span class="sxs-lookup"><span data-stu-id="908cc-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="908cc-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="908cc-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="908cc-156">Rendu des primitives</span><span class="sxs-lookup"><span data-stu-id="908cc-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
