---
description: Le rectangle englobant de toutes les analyses est l’écran virtuel. Le bureau couvre l’écran virtuel au lieu d’un seul moniteur. L’illustration suivante montre une organisation possible de trois analyses.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Écran virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991785"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="d3f49-105">Écran virtuel</span><span class="sxs-lookup"><span data-stu-id="d3f49-105">The Virtual Screen</span></span>

<span data-ttu-id="d3f49-106">Le rectangle englobant de toutes les analyses est l' *écran virtuel*.</span><span class="sxs-lookup"><span data-stu-id="d3f49-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="d3f49-107">Le bureau couvre l’écran virtuel au lieu d’un seul moniteur.</span><span class="sxs-lookup"><span data-stu-id="d3f49-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="d3f49-108">L’illustration suivante montre une organisation possible de trois analyses.</span><span class="sxs-lookup"><span data-stu-id="d3f49-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![Illustration montrant trois cases représentant les moniteurs organisés dans une zone représentant l’écran virtuel](images/multimon-1.png)

<span data-ttu-id="d3f49-110">L' *analyse principale* contient l’origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="d3f49-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="d3f49-111">Il s’agit d’une compatibilité avec les applications existantes qui attendent une analyse avec une origine.</span><span class="sxs-lookup"><span data-stu-id="d3f49-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="d3f49-112">Toutefois, il n’est pas nécessaire que l’analyse principale se trouve dans l’angle supérieur gauche de l’écran virtuel.</span><span class="sxs-lookup"><span data-stu-id="d3f49-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="d3f49-113">Dans la figure 1, il est proche du centre.</span><span class="sxs-lookup"><span data-stu-id="d3f49-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="d3f49-114">Lorsque l’analyse principale n’est pas en haut à gauche de l’écran virtuel, les parties de l’écran virtuel ont des coordonnées négatives.</span><span class="sxs-lookup"><span data-stu-id="d3f49-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="d3f49-115">Étant donné que la disposition des analyses est définie par l’utilisateur, toutes les applications doivent être conçues pour fonctionner avec des coordonnées négatives.</span><span class="sxs-lookup"><span data-stu-id="d3f49-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="d3f49-116">Pour plus d’informations, consultez [considérations relatives à la surveillance multiple pour les programmes plus anciens](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="d3f49-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="d3f49-117">Les coordonnées de l’écran virtuel sont représentées par une valeur 16 bits signée en raison des valeurs 16 bits contenues dans de nombreux messages existants.</span><span class="sxs-lookup"><span data-stu-id="d3f49-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="d3f49-118">Ainsi, les limites de l’écran virtuel sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3f49-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



