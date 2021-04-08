---
description: Les interfaces de rendu pour Direct3D consistent en des méthodes qui restituent des primitives à partir des données de vertex stockées dans une ou plusieurs mémoires tampons de données.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flux de données de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746101"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="0c9f6-103">Flux de données de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0c9f6-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="0c9f6-104">Les interfaces de rendu pour Direct3D consistent en des méthodes qui restituent des primitives à partir des données de vertex stockées dans une ou plusieurs mémoires tampons de données.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="0c9f6-105">Les données de vertex se composent d’éléments vertex combinés pour former des composants vertex.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="0c9f6-106">Les éléments vertex, la plus petite unité d’un vertex, représentent des entités telles que la position, la normale ou la couleur.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="0c9f6-107">Les composants vertex sont un ou plusieurs éléments de vertex stockés en continu (entrelacés par vertex) dans une mémoire tampon unique.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="0c9f6-108">Un vertex complet se compose d’un ou de plusieurs composants, où chaque composant se trouve dans une mémoire tampon distincte.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="0c9f6-109">Pour restituer une primitive, plusieurs composants vertex sont lus et assemblés afin que les vertex complets soient disponibles pour le traitement des vertex.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="0c9f6-110">Le diagramme suivant illustre le processus de rendu des primitives à l’aide de composants de vertex.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![diagramme du processus de rendu des primitives à l’aide de composants vertex](images/vertexdata.png)

<span data-ttu-id="0c9f6-112">Le rendu des primitives se compose de deux étapes.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="0c9f6-113">Tout d’abord, configurez un ou plusieurs flux de composants de vertex. Ensuite, appelez une méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pour effectuer le rendu à partir de ces flux.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="0c9f6-114">L’identification des éléments de vertex dans ces flux de composants est spécifiée par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="0c9f6-115">Les méthodes [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) spécifient un décalage dans les flux de données de vertex afin qu’un sous-ensemble contigu arbitraire des primitives dans un ensemble de données de vertex puisse être rendu avec chaque appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="0c9f6-116">Cela vous permet de modifier l’état de rendu de l’appareil entre des groupes de primitives qui sont restituées à partir des mêmes mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="0c9f6-117">Les méthodes de dessin indexées et non indexées sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="0c9f6-118">Pour plus d’informations, consultez [rendu à partir des mémoires tampons de vertex et d’index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0c9f6-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c9f6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c9f6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c9f6-120">Rendu des primitives</span><span class="sxs-lookup"><span data-stu-id="0c9f6-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
