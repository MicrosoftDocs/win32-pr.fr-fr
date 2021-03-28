---
description: Un polygone est une forme remplie avec des côtés droits.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: À propos des polygones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034233"
---
# <a name="about-polygons"></a><span data-ttu-id="9d158-103">À propos des polygones</span><span class="sxs-lookup"><span data-stu-id="9d158-103">About Polygons</span></span>

<span data-ttu-id="9d158-104">Un *polygone* est une forme remplie avec des côtés droits.</span><span class="sxs-lookup"><span data-stu-id="9d158-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="9d158-105">Les côtés d’un polygone sont dessinés à l’aide du stylet actuel.</span><span class="sxs-lookup"><span data-stu-id="9d158-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="9d158-106">Lorsque le système remplit un polygone, il utilise le pinceau actuel et le mode de remplissage polygone actuel.</span><span class="sxs-lookup"><span data-stu-id="9d158-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="9d158-107">Les deux modes de remplissage, alternatif (valeur par défaut) et enroulement, déterminent si les régions d’un polygone complexe sont remplies ou laissées non peintes.</span><span class="sxs-lookup"><span data-stu-id="9d158-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="9d158-108">Une application peut sélectionner l’un ou l’autre mode en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="9d158-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="9d158-109">Pour plus d’informations sur les modes de remplissage des polygones, consultez [régions](regions.md).</span><span class="sxs-lookup"><span data-stu-id="9d158-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="9d158-110">L’illustration suivante montre un polygone dessiné à l’aide de [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span><span class="sxs-lookup"><span data-stu-id="9d158-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![illustration d’un polygone dans la forme d’une étoile à cinq branches](images/csfsh-04.png)

<span data-ttu-id="9d158-112">En plus de dessiner un polygone unique à l’aide de [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), une application peut dessiner plusieurs polygones à l’aide de la fonction [**polypolygone**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .</span><span class="sxs-lookup"><span data-stu-id="9d158-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
