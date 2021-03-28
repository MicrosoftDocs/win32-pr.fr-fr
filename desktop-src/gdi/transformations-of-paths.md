---
description: Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformations de chemins d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973519"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="64bde-103">Transformations de chemins d’accès</span><span class="sxs-lookup"><span data-stu-id="64bde-103">Transformations of Paths</span></span>

<span data-ttu-id="64bde-104">Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles.</span><span class="sxs-lookup"><span data-stu-id="64bde-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="64bde-105">(Si la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) a été appelée, les unités logiques sont des unités universelles ; sinon, les unités logiques sont des unités de page.) Une application peut utiliser des transformations universelles pour mettre à l’échelle, faire pivoter, incliner, traduire et refléter les lignes et les courbes de Bézier qui définissent un tracé.</span><span class="sxs-lookup"><span data-stu-id="64bde-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="64bde-106">Une transformation universelle dans un crochet de chemin d’accès affecte uniquement les lignes et les courbes dessinées après la définition de la transformation.</span><span class="sxs-lookup"><span data-stu-id="64bde-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="64bde-107">Elle n’a aucun effet sur les lignes et les courbes qui ont été dessinées avant d’être définies.</span><span class="sxs-lookup"><span data-stu-id="64bde-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="64bde-108">Pour obtenir une description de la transformation universelle, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="64bde-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="64bde-109">Une application peut également utiliser [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour détailler la forme du stylet utilisé pour définir le contour d’un tracé si le stylet est un stylet géométrique.</span><span class="sxs-lookup"><span data-stu-id="64bde-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="64bde-110">Pour obtenir une description des plumes géométriques, consultez [stylets](pens.md).</span><span class="sxs-lookup"><span data-stu-id="64bde-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



