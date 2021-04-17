---
description: Un ventilateur triangulaire est semblable à une bande triangulaire, sauf que tous les triangles partagent un sommet, comme indiqué dans l’illustration suivante.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventilateurs triangulaires (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570465"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="80426-103">Ventilateurs triangulaires (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="80426-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="80426-104">Un ventilateur triangulaire est semblable à une bande triangulaire, sauf que tous les triangles partagent un sommet, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="80426-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![illustration d’un ventilateur triangulaire](images/trifan.gif)

<span data-ttu-id="80426-106">Le système utilise les vertex v2, v3 et V1 pour dessiner le premier triangle. v3, V4 et V1 pour dessiner le deuxième triangle ; v4, V5 et V1 pour dessiner le troisième triangle ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="80426-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="80426-107">Lorsque l’ombrage plat est activé, le système ombre le triangle avec la couleur de son premier vertex.</span><span class="sxs-lookup"><span data-stu-id="80426-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="80426-108">L’illustration suivante représente un ventilateur à triangle rendu.</span><span class="sxs-lookup"><span data-stu-id="80426-108">The following illustration depicts a rendered triangle fan.</span></span>

![illustration d’un ventilateur à triangle rendu](images/tfan2.gif)

<span data-ttu-id="80426-110">Le code suivant montre comment créer des vertex pour ce ventilateur de triangle.</span><span class="sxs-lookup"><span data-stu-id="80426-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="80426-111">L’exemple de code ci-dessous montre comment restituer ce ventilateur à triangle dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="80426-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="80426-112">Les ventilateurs de triangle ne sont pas pris en charge dans Direct3D 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="80426-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80426-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80426-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80426-114">Primitives</span><span class="sxs-lookup"><span data-stu-id="80426-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
