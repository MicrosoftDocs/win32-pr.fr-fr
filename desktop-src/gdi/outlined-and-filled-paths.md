---
description: Une application peut dessiner le contour d’un tracé en appelant la fonction StrokePath, elle peut remplir l’intérieur d’un tracé en appelant la fonction FillPath, et elle peut à la fois tracer et remplir le tracé en appelant la fonction StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Tracés détaillés et remplis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951554"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="d9288-103">Tracés détaillés et remplis</span><span class="sxs-lookup"><span data-stu-id="d9288-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="d9288-104">Une application peut dessiner le contour d’un tracé en appelant la fonction [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , elle peut remplir l’intérieur d’un tracé en appelant la fonction [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) , et elle peut à la fois tracer et remplir le tracé en appelant la fonction [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .</span><span class="sxs-lookup"><span data-stu-id="d9288-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="d9288-105">Chaque fois qu’une application remplit un chemin d’accès, le système utilise le mode de remplissage actuel du contrôleur de réseau.</span><span class="sxs-lookup"><span data-stu-id="d9288-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="d9288-106">Une application peut récupérer ce mode en appelant la fonction [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) , et elle peut définir un nouveau mode de remplissage en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="d9288-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="d9288-107">Pour obtenir une description des deux modes de remplissage, consultez [régions](regions.md).</span><span class="sxs-lookup"><span data-stu-id="d9288-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="d9288-108">L’illustration suivante montre la section transversale d’un objet créé par une application de conception assistée par ordinateur à l’aide de chemins d’accès qui ont été indiqués et remplis.</span><span class="sxs-lookup"><span data-stu-id="d9288-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![Illustration montrant la vue en plusieurs sections d’un objet, avec différentes parties indiquées par des motifs de remplissage différents](images/cspth-01.png)

 

 



