---
description: Étant donné une scène qui contient de nombreux objets qui utilisent la même géométrie, vous pouvez dessiner de nombreuses instances de cette géométrie à différentes orientations, tailles, couleurs, et ainsi de meilleures performances en réduisant la quantité de données que vous devez fournir au convertisseur.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Dessin efficace de plusieurs instances de Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845973"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="e0065-103">Dessin efficace de plusieurs instances de Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e0065-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="e0065-104">Étant donné une scène qui contient de nombreux objets qui utilisent la même géométrie, vous pouvez dessiner de nombreuses instances de cette géométrie à différentes orientations, tailles, couleurs, et ainsi de meilleures performances en réduisant la quantité de données que vous devez fournir au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="e0065-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="e0065-105">Pour ce faire, vous pouvez utiliser deux techniques : la première pour dessiner une géométrie indexée et la seconde pour une géométrie non indexée.</span><span class="sxs-lookup"><span data-stu-id="e0065-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="e0065-106">Les deux techniques utilisent deux mémoires tampons de vertex : une pour fournir les données géométriques et une pour fournir des données d’instance par objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="e0065-107">Les données d’instance peuvent être un large éventail d’informations, telles qu’une transformation, des données de couleur ou des données d’éclairage, en fait tout ce que vous pouvez décrire dans une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="e0065-108">Le dessin de nombreuses instances de Geometry avec ces techniques peut réduire considérablement la quantité de données envoyées au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="e0065-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="e0065-109">Dessin d’une géométrie indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="e0065-110">Comparaison des performances de la géométrie indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="e0065-111">Dessin de géométrie non indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="e0065-112">Comparaison des performances de la géométrie non indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="e0065-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0065-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="e0065-114">Dessin d’une géométrie indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="e0065-115">La mémoire tampon de vertex contient des données par vertex définies par une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="e0065-116">Supposons que la partie de chaque vertex contient des données géométriques et qu’une partie de chaque vertex contient des données d’instance par objet, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="e0065-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![diagramme d’une mémoire tampon de vertex pour une géométrie indexée](images/drawingmultipleinstances.png)

<span data-ttu-id="e0065-118">Cette technique nécessite un appareil qui prend en charge le \_ modèle de nuanceur de sommets 3 0.</span><span class="sxs-lookup"><span data-stu-id="e0065-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="e0065-119">Cette technique fonctionne avec n’importe quel nuanceur programmable, mais pas avec le pipeline de fonctions fixe.</span><span class="sxs-lookup"><span data-stu-id="e0065-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="e0065-120">Pour les mémoires tampons de vertex indiquées ci-dessus, Voici les déclarations de mémoire tampon de vertex correspondantes :</span><span class="sxs-lookup"><span data-stu-id="e0065-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="e0065-121">Ces déclarations définissent deux mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="e0065-122">La première déclaration (pour le flux 0, indiquée par les zéros de la colonne 1) définit les données geometry qui se composent des données de coordonnées : position, normal, tangente, Binormal et texture.</span><span class="sxs-lookup"><span data-stu-id="e0065-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="e0065-123">La deuxième déclaration (pour le flux 1, indiquée par celles de la colonne 1) définit les données de l’instance par objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="e0065-124">Chaque instance est définie par 4 4 chiffres à virgule flottante de composant et une couleur à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="e0065-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="e0065-125">Les quatre premières valeurs peuvent être utilisées pour initialiser une matrice 4x4, ce qui signifie que ces données sont dimensionnées de manière unique, positionnent et font pivoter chaque instance de la géométrie.</span><span class="sxs-lookup"><span data-stu-id="e0065-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="e0065-126">Les quatre premiers composants utilisent une sémantique de coordonnée de texture qui, dans ce cas, signifie « il s’agit d’un nombre général de quatre composants ».</span><span class="sxs-lookup"><span data-stu-id="e0065-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="e0065-127">Lorsque vous utilisez des données arbitraires dans une déclaration de vertex, utilisez une sémantique de coordonnée de texture pour la marquer.</span><span class="sxs-lookup"><span data-stu-id="e0065-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="e0065-128">Le dernier élément du flux est utilisé pour les données de couleur.</span><span class="sxs-lookup"><span data-stu-id="e0065-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="e0065-129">Cela peut être appliqué au nuanceur de sommets pour attribuer à chaque instance une couleur unique.</span><span class="sxs-lookup"><span data-stu-id="e0065-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="e0065-130">Avant le rendu, vous devez appeler [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) pour lier les flux de mémoire tampon de vertex à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e0065-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="e0065-131">Voici un exemple qui lie les deux mémoires tampons de vertex :</span><span class="sxs-lookup"><span data-stu-id="e0065-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="e0065-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilise [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) pour identifier les données géométriques indexées.</span><span class="sxs-lookup"><span data-stu-id="e0065-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="e0065-133">Dans ce cas, le flux 0 contient les données indexées qui décrivent la géométrie de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="e0065-134">Cette valeur est associée logiquement au nombre d’instances de la géométrie à dessiner.</span><span class="sxs-lookup"><span data-stu-id="e0065-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="e0065-135">Notez que D3DSTREAMSOURCE \_ INDEXEDDATA et le nombre d’instances à dessiner doivent toujours être définis dans le flux zéro.</span><span class="sxs-lookup"><span data-stu-id="e0065-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="e0065-136">Dans le deuxième appel, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilise [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) pour identifier le flux contenant les données d’instance.</span><span class="sxs-lookup"><span data-stu-id="e0065-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="e0065-137">Cette valeur est associée de manière logique à 1, car chaque vertex contient un jeu de données d’instance.</span><span class="sxs-lookup"><span data-stu-id="e0065-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="e0065-138">Les deux derniers appels à [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lient les pointeurs de tampon de vertex à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e0065-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="e0065-139">Lorsque vous avez terminé de restituer les données de l’instance, veillez à réinitialiser la fréquence du flux du vertex à son état par défaut (qui n’utilise pas l’instanciation).</span><span class="sxs-lookup"><span data-stu-id="e0065-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="e0065-140">Étant donné que cet exemple utilise deux flux, définissez les deux flux comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e0065-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="e0065-141">Comparaison des performances de la géométrie indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="e0065-142">Bien qu’il ne soit pas possible d’effectuer une seule conclusion sur l’ampleur de cette technique pour réduire le temps de rendu dans chaque application, considérez la différence entre la quantité de données transmises dans le runtime et le nombre de modifications d’État qui seront réduites si vous utilisez la technique d’instanciation.</span><span class="sxs-lookup"><span data-stu-id="e0065-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="e0065-143">Cette séquence de rendu tire parti du dessin de plusieurs instances de la même géométrie :</span><span class="sxs-lookup"><span data-stu-id="e0065-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="e0065-144">Notez que la boucle de rendu est appelée une fois, que les données geometry sont diffusées une seule fois, et que n instances sont transmises en continu une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e0065-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="e0065-145">Cette séquence de rendu suivante est identique dans les fonctionnalités, mais ne tire pas parti de l’instanciation :</span><span class="sxs-lookup"><span data-stu-id="e0065-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="e0065-146">Notez que l’intégralité de la boucle de rendu est encapsulée par une seconde boucle pour dessiner chaque objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="e0065-147">Désormais, les données géométriques sont diffusées dans le convertisseur n fois (au lieu d’une fois) et tous les États de pipeline peuvent également être définis de manière redondante pour chaque objet dessiné.</span><span class="sxs-lookup"><span data-stu-id="e0065-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="e0065-148">Cette séquence de rendu est très susceptible d’être beaucoup plus lente.</span><span class="sxs-lookup"><span data-stu-id="e0065-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="e0065-149">Notez également que les paramètres de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) n’ont pas changé entre les deux boucles de rendu.</span><span class="sxs-lookup"><span data-stu-id="e0065-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="e0065-150">Dessin de géométrie non indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="e0065-151">Dans le [dessin de géométrie indexée](#drawing-indexed-geometry), les mémoires tampons de vertex ont été configurées pour dessiner plusieurs instances de géométrie indexée avec une plus grande efficacité.</span><span class="sxs-lookup"><span data-stu-id="e0065-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="e0065-152">Vous pouvez également utiliser [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) pour dessiner une géométrie non indexée.</span><span class="sxs-lookup"><span data-stu-id="e0065-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="e0065-153">Cela nécessite une disposition de mémoire tampon de vertex différente et a des contraintes différentes.</span><span class="sxs-lookup"><span data-stu-id="e0065-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="e0065-154">Pour dessiner une géométrie non indexée, préparez vos mémoires tampons de vertex comme dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="e0065-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![diagramme d’une mémoire tampon de vertex pour une géométrie non indexée](images/olderstyleinstancing.png)

<span data-ttu-id="e0065-156">Cette technique n’est pas prise en charge par l’accélération matérielle sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e0065-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="e0065-157">Il est uniquement pris en charge par le traitement du vertex logiciel et ne fonctionne qu’avec les nuanceurs [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .</span><span class="sxs-lookup"><span data-stu-id="e0065-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="e0065-158">Étant donné que cette technique fonctionne avec une géométrie non indexée, il n’y a pas de mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="e0065-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="e0065-159">Comme le montre le diagramme, la mémoire tampon de vertex qui contient Geometry contient n copies des données geometry.</span><span class="sxs-lookup"><span data-stu-id="e0065-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="e0065-160">Pour chaque instance dessinée, les données de géométrie sont lues à partir de la première mémoire tampon de vertex et les données d’instance sont lues à partir de la deuxième mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="e0065-161">Les déclarations de mémoire tampon de vertex correspondantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0065-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="e0065-162">Ces déclarations sont identiques aux déclarations effectuées dans l’exemple de géométrie indexée.</span><span class="sxs-lookup"><span data-stu-id="e0065-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="e0065-163">Là encore, la première déclaration (pour Stream 0) définit les données geometry et la deuxième déclaration (pour Stream 1) définit les données d’instance par objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="e0065-164">Lorsque vous créez la première mémoire tampon de vertex, veillez à la charger avec le nombre d’instances des données geometry que vous dessinerez.</span><span class="sxs-lookup"><span data-stu-id="e0065-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="e0065-165">Avant le rendu, vous devez configurer le séparateur qui indique au runtime comment diviser la première mémoire tampon vertex en n instances.</span><span class="sxs-lookup"><span data-stu-id="e0065-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="e0065-166">Définissez ensuite le diviseur à l’aide de [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) comme suit :</span><span class="sxs-lookup"><span data-stu-id="e0065-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="e0065-167">Le premier appel à [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indique que le flux 0 contient n instances de m vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="e0065-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lie ensuite le flux 0 à la mémoire tampon de vertex Geometry.</span><span class="sxs-lookup"><span data-stu-id="e0065-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="e0065-169">Dans le deuxième appel, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifie le flux 1 comme la source des données de l’instance.</span><span class="sxs-lookup"><span data-stu-id="e0065-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="e0065-170">Le deuxième paramètre est le nombre de vertex dans chaque objet (m).</span><span class="sxs-lookup"><span data-stu-id="e0065-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="e0065-171">N’oubliez pas que le flux de données de l’instance doit toujours être déclaré comme second flux.</span><span class="sxs-lookup"><span data-stu-id="e0065-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="e0065-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lie ensuite le flux 1 à la mémoire tampon de vertex qui contient les données d’instance.</span><span class="sxs-lookup"><span data-stu-id="e0065-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="e0065-173">Lorsque vous avez terminé de restituer les données d’instance, veillez à rétablir l’État par défaut de la fréquence du flux de vertex.</span><span class="sxs-lookup"><span data-stu-id="e0065-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="e0065-174">Étant donné que cet exemple utilise deux flux, définissez les deux flux comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e0065-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="e0065-175">Comparaison des performances de la géométrie non indexée</span><span class="sxs-lookup"><span data-stu-id="e0065-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="e0065-176">Le principal avantage de ce style d’instanciation est qu’il peut être utilisé sur une géométrie non indexée.</span><span class="sxs-lookup"><span data-stu-id="e0065-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="e0065-177">Bien qu’il ne soit pas possible d’effectuer une seule conclusion sur l’ampleur de cette technique pour réduire le temps de rendu dans chaque application, considérez la différence entre la quantité de données transmises dans le runtime et le nombre de modifications d’État qui seront réduites pour la séquence de rendu suivante :</span><span class="sxs-lookup"><span data-stu-id="e0065-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="e0065-178">Notez que la boucle de rendu est appelée une fois.</span><span class="sxs-lookup"><span data-stu-id="e0065-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="e0065-179">Les données geometry sont diffusées une seule fois, même si n instances de la géométrie sont diffusées en continu.</span><span class="sxs-lookup"><span data-stu-id="e0065-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="e0065-180">Les données de la mémoire tampon de vertex d’instance sont diffusées une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e0065-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="e0065-181">Cette séquence de rendu suivante est identique dans les fonctionnalités, mais ne tire pas parti de l’instanciation :</span><span class="sxs-lookup"><span data-stu-id="e0065-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="e0065-182">Sans instanciation, la boucle de rendu doit être encapsulée par une seconde boucle pour dessiner chaque objet.</span><span class="sxs-lookup"><span data-stu-id="e0065-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="e0065-183">En éliminant la deuxième boucle de rendu, vous devez obtenir de meilleures performances en raison de moins de modifications d’état de rendu appelées à l’intérieur de la boucle.</span><span class="sxs-lookup"><span data-stu-id="e0065-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="e0065-184">Globalement, il est raisonnable de s’attendre à ce que la technique indexée ([dessin de géométrie indexée](#drawing-indexed-geometry)) soit plus performante que la technique non indexée ([dessinant une géométrie non indexée](#drawing-non-indexed-geometry)), car la technique indexée diffuse uniquement une copie des données geometry.</span><span class="sxs-lookup"><span data-stu-id="e0065-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="e0065-185">Notez que les paramètres de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) n’ont pas changé pour l’une des séquences de rendu.</span><span class="sxs-lookup"><span data-stu-id="e0065-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0065-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0065-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0065-187">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="e0065-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="e0065-188">[Exemple d’instanciation](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e0065-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
