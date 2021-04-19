---
description: Une bande est une primitive composée de segments de ligne connectés.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Bandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521951"
---
# <a name="line-strips"></a><span data-ttu-id="df531-103">Bandes</span><span class="sxs-lookup"><span data-stu-id="df531-103">Line Strips</span></span>

<span data-ttu-id="df531-104">Une bande est une primitive composée de segments de ligne connectés.</span><span class="sxs-lookup"><span data-stu-id="df531-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="df531-105">Votre application peut utiliser des bandes de lignes pour créer des polygones qui ne sont pas fermés.</span><span class="sxs-lookup"><span data-stu-id="df531-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="df531-106">Un polygone fermé est un polygone dont le dernier vertex est connecté à son premier vertex par un segment de ligne.</span><span class="sxs-lookup"><span data-stu-id="df531-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="df531-107">Si votre application crée des polygones basés sur des bandes, il n’est pas garanti que les vertex soient coplanés.</span><span class="sxs-lookup"><span data-stu-id="df531-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="df531-108">L’illustration suivante montre une bande de lignes rendue.</span><span class="sxs-lookup"><span data-stu-id="df531-108">The following illustration shows a rendered line strip.</span></span>

![illustration d’une bande](images/linstrip.gif)

<span data-ttu-id="df531-110">Le code suivant montre comment créer des sommets pour cette bande.</span><span class="sxs-lookup"><span data-stu-id="df531-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="df531-111">L’exemple de code ci-dessous montre comment afficher une bande de courbes dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="df531-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="df531-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df531-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df531-113">Primitives</span><span class="sxs-lookup"><span data-stu-id="df531-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
