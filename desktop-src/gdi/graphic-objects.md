---
description: Le stylet, le pinceau, la bitmap, la palette, la région et le chemin d’accès associés à un contrôleur de périphérique sont appelés objets graphiques. Les attributs suivants sont associés à chacun de ces objets.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objets graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991216"
---
# <a name="graphic-objects"></a><span data-ttu-id="6fff8-104">Objets graphiques</span><span class="sxs-lookup"><span data-stu-id="6fff8-104">Graphic Objects</span></span>

<span data-ttu-id="6fff8-105">Le stylet, le pinceau, la bitmap, la palette, la région et le chemin d’accès associés à un contrôleur de périphérique sont appelés objets graphiques.</span><span class="sxs-lookup"><span data-stu-id="6fff8-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="6fff8-106">Les attributs suivants sont associés à chacun de ces objets.</span><span class="sxs-lookup"><span data-stu-id="6fff8-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="6fff8-107">Objet graphique</span><span class="sxs-lookup"><span data-stu-id="6fff8-107">Graphic object</span></span> | <span data-ttu-id="6fff8-108">Attributs associés</span><span class="sxs-lookup"><span data-stu-id="6fff8-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6fff8-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="6fff8-109">Bitmap</span></span>         | <span data-ttu-id="6fff8-110">Taille, en octets ; Dimensions, en pixels ; format de couleur ; schéma de compression ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6fff8-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="6fff8-111">Brush</span><span class="sxs-lookup"><span data-stu-id="6fff8-111">Brush</span></span>          | <span data-ttu-id="6fff8-112">Style, couleur, motif et origine.</span><span class="sxs-lookup"><span data-stu-id="6fff8-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="6fff8-113">Palette</span><span class="sxs-lookup"><span data-stu-id="6fff8-113">Palette</span></span>        | <span data-ttu-id="6fff8-114">Couleurs et taille (ou nombre de couleurs).</span><span class="sxs-lookup"><span data-stu-id="6fff8-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="6fff8-115">Police</span><span class="sxs-lookup"><span data-stu-id="6fff8-115">Font</span></span>           | <span data-ttu-id="6fff8-116">Nom de la police, largeur, hauteur, poids, jeu de caractères, etc.</span><span class="sxs-lookup"><span data-stu-id="6fff8-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="6fff8-117">Path</span><span class="sxs-lookup"><span data-stu-id="6fff8-117">Path</span></span>           | <span data-ttu-id="6fff8-118">Automatiques.</span><span class="sxs-lookup"><span data-stu-id="6fff8-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="6fff8-119">Stylet</span><span class="sxs-lookup"><span data-stu-id="6fff8-119">Pen</span></span>            | <span data-ttu-id="6fff8-120">Style, largeur et couleur.</span><span class="sxs-lookup"><span data-stu-id="6fff8-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="6fff8-121">Région</span><span class="sxs-lookup"><span data-stu-id="6fff8-121">Region</span></span>         | <span data-ttu-id="6fff8-122">Emplacement et dimensions.</span><span class="sxs-lookup"><span data-stu-id="6fff8-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="6fff8-123">Quand une application crée un contrôleur de réseau, le système stocke automatiquement un ensemble d’objets par défaut dans celui-ci (il n’y a pas de bitmap ou de chemin d’accès par défaut).</span><span class="sxs-lookup"><span data-stu-id="6fff8-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="6fff8-124">Une application peut examiner les attributs des objets par défaut en appelant les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="6fff8-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="6fff8-125">L’application peut modifier ces valeurs par défaut en créant un nouvel objet et en le sélectionnant dans le DC.</span><span class="sxs-lookup"><span data-stu-id="6fff8-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="6fff8-126">Un objet est sélectionné dans un DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="6fff8-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="6fff8-127">Une application peut définir la couleur de pinceau actuelle sur une valeur de couleur spécifiée avec [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span><span class="sxs-lookup"><span data-stu-id="6fff8-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="6fff8-128">La fonction [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) retourne la couleur du pinceau DC.</span><span class="sxs-lookup"><span data-stu-id="6fff8-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="6fff8-129">La fonction [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) définit la couleur du stylet sur une valeur de couleur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6fff8-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="6fff8-130">La fonction [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) retourne la couleur du stylet DC.</span><span class="sxs-lookup"><span data-stu-id="6fff8-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



