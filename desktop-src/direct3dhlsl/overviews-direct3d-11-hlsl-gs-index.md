---
title: Comment indexer plusieurs flux de sortie
description: Dans le nuancier Model 5, un nuanceur Geometry peut prendre en charge jusqu’à 4 flux distincts. Cela signifie qu’un seul nuanceur peut sortir d’un à quatre flux de sortie, selon le nombre de flux déclarés.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028683"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="33820-104">Comment : indexer plusieurs flux de sortie</span><span class="sxs-lookup"><span data-stu-id="33820-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="33820-105">Dans le nuancier Model 5, un nuanceur Geometry peut prendre en charge jusqu’à 4 flux distincts.</span><span class="sxs-lookup"><span data-stu-id="33820-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="33820-106">Cela signifie qu’un seul nuanceur peut sortir d’un à quatre flux de sortie, selon le nombre de flux déclarés.</span><span class="sxs-lookup"><span data-stu-id="33820-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="33820-107">Pour indexer plusieurs flux de sortie</span><span class="sxs-lookup"><span data-stu-id="33820-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="33820-108">Définissez un flux de données à l’aide d’un type de modèle de flux.</span><span class="sxs-lookup"><span data-stu-id="33820-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="33820-109">Définissez un deuxième flux de données à l’aide d’un type de modèle de flux.</span><span class="sxs-lookup"><span data-stu-id="33820-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="33820-110">Données de sortie pour les flux (ou les deux) à l’aide des fonctions intrinsèques de l’objet de sortie de flux (par exemple, Append ou RestartStrip).</span><span class="sxs-lookup"><span data-stu-id="33820-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="33820-111">Lorsque vous utilisez un seul flux de sortie, vous pouvez émettre des franges de triangle, des bandes ou des listes de points.</span><span class="sxs-lookup"><span data-stu-id="33820-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="33820-112">Lorsque vous stockez des bandes triangulaires et des franges dans le tampon de sortie de flux, elles sont développées respectivement en triangle et en listes de lignes.</span><span class="sxs-lookup"><span data-stu-id="33820-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="33820-113">Vous pouvez également pixelliser un flux et ne pas l’envoyer à une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="33820-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="33820-114">Lorsque vous utilisez plusieurs flux de sortie, tous les flux doivent contenir des points, et un flux de sortie jusqu’à un peut être envoyé au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="33820-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="33820-115">Plus généralement, une application ne pixellise aucun flux.</span><span class="sxs-lookup"><span data-stu-id="33820-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="33820-116">Une fois que vous avez diffusé des données dans une mémoire tampon, vous pouvez utiliser ces données pour restituer n’importe quel type primitif, pas seulement le type primitif que vous avez utilisé pour remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="33820-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="33820-117">La sortie totale du nuanceur Geometry est limitée à 1024 scalaires.</span><span class="sxs-lookup"><span data-stu-id="33820-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="33820-118">Lorsque plusieurs flux existent, le nombre de scalaires est calculé à partir du plus grand type de flux multiplié par le nombre maximal de vertex.</span><span class="sxs-lookup"><span data-stu-id="33820-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33820-119">Différences entre le Shader Model 4 et le Shader Model 5 :</span><span class="sxs-lookup"><span data-stu-id="33820-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="33820-120">Nuanceur modèle 4 :</span><span class="sxs-lookup"><span data-stu-id="33820-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="33820-121">Le nombre maximal de scalaires pour la sortie du flux est de 64.</span><span class="sxs-lookup"><span data-stu-id="33820-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="33820-122">Le masque de Registre par composant doit correspondre dans la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="33820-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="33820-123">Nuancier modèle 5 :</span><span class="sxs-lookup"><span data-stu-id="33820-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="33820-124">Le nombre maximal de scalaires pour la sortie du flux est de 128.</span><span class="sxs-lookup"><span data-stu-id="33820-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="33820-125">Le masque de Registre par composant ne doit pas nécessairement correspondre à la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="33820-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="33820-126">L’indexation dynamique des sorties doit être légale sur tous les flux.</span><span class="sxs-lookup"><span data-stu-id="33820-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="33820-127">Les modes d’interpolation n’ont pas besoin d’être identiques pour les flux.</span><span class="sxs-lookup"><span data-stu-id="33820-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="33820-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33820-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33820-129">Fonctionnalités du nuanceur Geometry</span><span class="sxs-lookup"><span data-stu-id="33820-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





