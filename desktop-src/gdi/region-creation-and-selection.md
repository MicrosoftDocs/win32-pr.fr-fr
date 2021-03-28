---
description: Une application crée une région en appelant une fonction associée à une forme spécifique. Le tableau suivant indique la ou les fonctions associées à chacune des formes standard.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Création et sélection de régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972547"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="78747-104">Création et sélection de régions</span><span class="sxs-lookup"><span data-stu-id="78747-104">Region Creation and Selection</span></span>

<span data-ttu-id="78747-105">Une application crée une région en appelant une fonction associée à une forme spécifique.</span><span class="sxs-lookup"><span data-stu-id="78747-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="78747-106">Le tableau suivant indique la ou les fonctions associées à chacune des formes standard.</span><span class="sxs-lookup"><span data-stu-id="78747-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="78747-107">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="78747-107">Shape</span></span>                                   | <span data-ttu-id="78747-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="78747-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78747-109">Zone rectangulaire</span><span class="sxs-lookup"><span data-stu-id="78747-109">Rectangular region</span></span>                      | <span data-ttu-id="78747-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="78747-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="78747-111">Zone rectangulaire avec angles arrondis</span><span class="sxs-lookup"><span data-stu-id="78747-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="78747-112">**CreateRoundRectRgn**</span><span class="sxs-lookup"><span data-stu-id="78747-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="78747-113">Région elliptique</span><span class="sxs-lookup"><span data-stu-id="78747-113">Elliptical region</span></span>                       | <span data-ttu-id="78747-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="78747-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="78747-115">Région polygonale</span><span class="sxs-lookup"><span data-stu-id="78747-115">Polygonal region</span></span>                        | <span data-ttu-id="78747-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="78747-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="78747-117">Chaque fonction de création de région retourne un handle qui identifie la nouvelle région.</span><span class="sxs-lookup"><span data-stu-id="78747-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="78747-118">Une application peut utiliser ce handle pour sélectionner la région dans un contexte de périphérique en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) et en fournissant ce handle comme deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="78747-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="78747-119">Une fois qu’une région est sélectionnée dans un contexte de périphérique, l’application peut effectuer diverses opérations sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="78747-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



