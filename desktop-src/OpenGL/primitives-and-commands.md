---
title: Primitives et commandes
description: Primitives et commandes
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, Primitives
- OpenGL, commandes
- primitives OpenGL
- commandes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672506"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="108c1-107">Primitives et commandes</span><span class="sxs-lookup"><span data-stu-id="108c1-107">Primitives and Commands</span></span>

<span data-ttu-id="108c1-108">OpenGL dessine des points de *primitives* , des segments de ligne ou des polygonssubject à plusieurs modes sélectionnables.</span><span class="sxs-lookup"><span data-stu-id="108c1-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="108c1-109">Vous pouvez contrôler les modes indépendamment l’un de l’autre.</span><span class="sxs-lookup"><span data-stu-id="108c1-109">You can control modes independently of one another.</span></span> <span data-ttu-id="108c1-110">Autrement dit, la définition d’un mode n’affecte pas l’ensemble des modes (même si de nombreux modes peuvent interagir pour déterminer ce qui finit par se terminer dans le trame).</span><span class="sxs-lookup"><span data-stu-id="108c1-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="108c1-111">Pour spécifier des primitives, définir des modes et exécuter d’autres opérations OpenGL, vous émettez des commandes sous la forme d’appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="108c1-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="108c1-112">Les primitives sont définies par un groupe d’un ou de plusieurs *vertex*.</span><span class="sxs-lookup"><span data-stu-id="108c1-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="108c1-113">Un vertex définit un point, un point de terminaison d’une ligne ou un angle d’un polygone où deux bords se rencontrent.</span><span class="sxs-lookup"><span data-stu-id="108c1-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="108c1-114">Les données (composées de coordonnées de vertex, de couleurs, de normales, de coordonnées de texture et d’indicateurs de périphérie) sont associées à un vertex, et chaque vertex et ses données associées sont traités indépendamment, dans l’ordre et de la même façon.</span><span class="sxs-lookup"><span data-stu-id="108c1-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="108c1-115">Les seules exceptions à cette règle sont les cas dans lesquels le groupe de vertex doit être coupé afin qu’une primitive particulière tienne dans une région spécifiée.</span><span class="sxs-lookup"><span data-stu-id="108c1-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="108c1-116">Dans ce cas, les données de vertex peuvent être modifiées et de nouveaux vertex créés.</span><span class="sxs-lookup"><span data-stu-id="108c1-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="108c1-117">Le type de découpage dépend de la primitive représentée par le groupe de vertex.</span><span class="sxs-lookup"><span data-stu-id="108c1-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="108c1-118">Les commandes sont toujours traitées dans l’ordre dans lequel elles sont reçues, bien qu’il puisse y avoir un délai indéterminé avant que la commande prenne effet.</span><span class="sxs-lookup"><span data-stu-id="108c1-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="108c1-119">Cela signifie que chaque primitive est entièrement dessinée avant que toute commande suivante prenne effet.</span><span class="sxs-lookup"><span data-stu-id="108c1-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="108c1-120">Cela signifie également que les commandes d’interrogation d’État renvoient des données cohérentes avec l’exécution complète de toutes les commandes OpenGL précédemment émises.</span><span class="sxs-lookup"><span data-stu-id="108c1-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




