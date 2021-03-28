---
description: Les dimensions d’un stylet géométrique sont spécifiées en unités logiques.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Stylos géométriques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991221"
---
# <a name="geometric-pens"></a><span data-ttu-id="894d7-103">Stylos géométriques</span><span class="sxs-lookup"><span data-stu-id="894d7-103">Geometric Pens</span></span>

<span data-ttu-id="894d7-104">Les dimensions d’un stylet géométrique sont spécifiées en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="894d7-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="894d7-105">Par conséquent, les lignes dessinées avec un stylet géométrique peuvent être mises à l’échelle, car elles peuvent apparaître plus larges ou plus étroites, selon la transformation universelle actuelle.</span><span class="sxs-lookup"><span data-stu-id="894d7-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="894d7-106">Pour plus d’informations sur la transformation universelle, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="894d7-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="894d7-107">Outre les trois attributs partagés avec des plumes cosmétiques (largeur, style et couleur), les plumes géométriques possèdent les quatre attributs suivants : modèle, hachage facultatif, style de fin et style de jointure.</span><span class="sxs-lookup"><span data-stu-id="894d7-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="894d7-108">Pour plus d’informations sur ces attributs, consultez [Pen Attributes](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="894d7-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="894d7-109">Pour créer un stylet géométrique, une application utilise la fonction [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="894d7-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="894d7-110">Comme avec les plumes cosmétiques, la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) sélectionne un stylet géométrique dans le contrôleur de l’application.</span><span class="sxs-lookup"><span data-stu-id="894d7-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



