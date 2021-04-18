---
description: Une famille de polices est un ensemble de polices ayant des caractéristiques de largeur de trait et d’empattement communes. Il existe cinq familles de polices. Une sixième famille permet à une application d’utiliser la police par défaut. Le tableau suivant décrit les familles de polices.
ms.assetid: 3c462000-4f65-43d0-8937-059081a8c417
title: Familles de polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfda200967b5efbf773fadc17d5093a856d0317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991232"
---
# <a name="font-families"></a><span data-ttu-id="f124b-106">Familles de polices</span><span class="sxs-lookup"><span data-stu-id="f124b-106">Font Families</span></span>

<span data-ttu-id="f124b-107">Une *famille de polices* est un ensemble de polices ayant des caractéristiques de largeur de trait et d’empattement communes.</span><span class="sxs-lookup"><span data-stu-id="f124b-107">A *font family* is a set of fonts having common stroke width and serif characteristics.</span></span> <span data-ttu-id="f124b-108">Il existe cinq familles de polices.</span><span class="sxs-lookup"><span data-stu-id="f124b-108">There are five font families.</span></span> <span data-ttu-id="f124b-109">Une sixième famille permet à une application d’utiliser la police par défaut.</span><span class="sxs-lookup"><span data-stu-id="f124b-109">A sixth family allows an application to use the default font.</span></span> <span data-ttu-id="f124b-110">Le tableau suivant décrit les familles de polices.</span><span class="sxs-lookup"><span data-stu-id="f124b-110">The following table describes the font-families.</span></span>



| <span data-ttu-id="f124b-111">Famille de polices</span><span class="sxs-lookup"><span data-stu-id="f124b-111">Font family</span></span> | <span data-ttu-id="f124b-112">Description</span><span class="sxs-lookup"><span data-stu-id="f124b-112">Description</span></span>                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f124b-113">Décoratif</span><span class="sxs-lookup"><span data-stu-id="f124b-113">Decorative</span></span>  | <span data-ttu-id="f124b-114">Spécifie une police fantaisie.</span><span class="sxs-lookup"><span data-stu-id="f124b-114">Specifies a novelty font.</span></span> <span data-ttu-id="f124b-115">Par exemple, l’ancien est l’anglais.</span><span class="sxs-lookup"><span data-stu-id="f124b-115">An example is Old English.</span></span>                                                                                          |
| <span data-ttu-id="f124b-116">Dontcare</span><span class="sxs-lookup"><span data-stu-id="f124b-116">Dontcare</span></span>    | <span data-ttu-id="f124b-117">Spécifie un nom de famille générique.</span><span class="sxs-lookup"><span data-stu-id="f124b-117">Specifies a generic family name.</span></span> <span data-ttu-id="f124b-118">Ce nom est utilisé lorsque les informations sur une police n’existent pas ou n’ont pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="f124b-118">This name is used when information about a font does not exist or does not matter.</span></span> <span data-ttu-id="f124b-119">La police par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f124b-119">The default font is used.</span></span> |
| <span data-ttu-id="f124b-120">Moderne</span><span class="sxs-lookup"><span data-stu-id="f124b-120">Modern</span></span>      | <span data-ttu-id="f124b-121">Spécifie une police à espacement fixe avec ou sans empattements.</span><span class="sxs-lookup"><span data-stu-id="f124b-121">Specifies a monospace font with or without serifs.</span></span> <span data-ttu-id="f124b-122">Les polices à espacement fixe sont généralement modernes ; les exemples sont PICA, Elite et Courier New.</span><span class="sxs-lookup"><span data-stu-id="f124b-122">Monospace fonts are usually modern; examples include Pica, Elite, and Courier New.</span></span>         |
| <span data-ttu-id="f124b-123">$</span><span class="sxs-lookup"><span data-stu-id="f124b-123">Roman</span></span>       | <span data-ttu-id="f124b-124">Spécifie une police proportionnelle avec empattements.</span><span class="sxs-lookup"><span data-stu-id="f124b-124">Specifies a proportional font with serifs.</span></span> <span data-ttu-id="f124b-125">Par exemple, Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="f124b-125">An example is Times New Roman.</span></span>                                                                     |
| <span data-ttu-id="f124b-126">Script</span><span class="sxs-lookup"><span data-stu-id="f124b-126">Script</span></span>      | <span data-ttu-id="f124b-127">Spécifie une police conçue pour ressembler à l’écriture manuscrite. exemples : script et Cursive.</span><span class="sxs-lookup"><span data-stu-id="f124b-127">Specifies a font that is designed to look like handwriting; examples include Script and Cursive.</span></span>                                              |
| <span data-ttu-id="f124b-128">Suisse</span><span class="sxs-lookup"><span data-stu-id="f124b-128">Swiss</span></span>       | <span data-ttu-id="f124b-129">Spécifie une police proportionnelle sans serifs.</span><span class="sxs-lookup"><span data-stu-id="f124b-129">Specifies a proportional font without serifs.</span></span> <span data-ttu-id="f124b-130">Par exemple, Arial.</span><span class="sxs-lookup"><span data-stu-id="f124b-130">An example is Arial.</span></span>                                                                            |



 

<span data-ttu-id="f124b-131">Ces familles de polices correspondent à des constantes trouvées dans le fichier WinGDI. h : FF \_ décoratif, FF \_ dontcare, FF \_ moderne, FF \_ roman, FF \_ script et FF \_ Suisse.</span><span class="sxs-lookup"><span data-stu-id="f124b-131">These font families correspond to constants found in the Wingdi.h file: FF\_DECORATIVE, FF\_DONTCARE, FF\_MODERN, FF\_ROMAN, FF\_SCRIPT, and FF\_SWISS.</span></span> <span data-ttu-id="f124b-132">Une application utilise ces constantes lorsqu’elle crée une police, sélectionne une police ou récupère des informations sur une police.</span><span class="sxs-lookup"><span data-stu-id="f124b-132">An application uses these constants when it creates a font, selects a font, or retrieves information about a font.</span></span>

<span data-ttu-id="f124b-133">Les polices au sein d’une famille se distinguent par leur taille (10 points, 24 points, etc.) et le style (normal, italique, etc.).</span><span class="sxs-lookup"><span data-stu-id="f124b-133">Fonts within a family are distinguished by size (10 point, 24 point, and so on) and style (regular, italic, and so on).</span></span>

 

 



