---
title: Macros pour les valeurs et couleurs CMJN
description: Les macros suivantes sont utiles pour manipuler des valeurs CMJN.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), macros CMJN
- WCS (Windows Color System), macros CMJN
- gestion des couleurs des images, macros CMJN
- gestion des couleurs, macros CMJN
- couleurs, macros CMJN
- Référence WCS, macros CMJN
- référence pour les macros WCS, CMJN
- Macros CMJN
- cyan magenta jaune noir (CMJN)
- CMJN (cyan magenta jaune noir)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106538414"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="fc105-113">Macros pour les valeurs et couleurs CMJN</span><span class="sxs-lookup"><span data-stu-id="fc105-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="fc105-114">Les macros suivantes sont utiles pour manipuler des valeurs CMJN.</span><span class="sxs-lookup"><span data-stu-id="fc105-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="fc105-115">Macro</span><span class="sxs-lookup"><span data-stu-id="fc105-115">Macro</span></span>                          | <span data-ttu-id="fc105-116">Description</span><span class="sxs-lookup"><span data-stu-id="fc105-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="fc105-117">**CMJN**</span><span class="sxs-lookup"><span data-stu-id="fc105-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="fc105-118">Crée une valeur CMJN à partir de valeurs cyan, magenta, jaune et noir individuelles.</span><span class="sxs-lookup"><span data-stu-id="fc105-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="fc105-119">**GetCValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="fc105-120">Récupère la valeur de couleur cyan à partir d’une valeur de couleur CMJN.</span><span class="sxs-lookup"><span data-stu-id="fc105-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="fc105-121">**GetKValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="fc105-122">Récupère la valeur de couleur noire à partir d’une valeur de couleur CMJN.</span><span class="sxs-lookup"><span data-stu-id="fc105-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="fc105-123">**GetMValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="fc105-124">Récupère la valeur magenta à partir d’une valeur de couleur CMJN.</span><span class="sxs-lookup"><span data-stu-id="fc105-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="fc105-125">**GetYValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="fc105-126">Récupère la valeur de couleur jaune à partir d’une valeur de couleur CMJN.</span><span class="sxs-lookup"><span data-stu-id="fc105-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="fc105-127">Les macros suivantes sont utilisées avec des couleurs.</span><span class="sxs-lookup"><span data-stu-id="fc105-127">The following macros are used with color.</span></span>



| <span data-ttu-id="fc105-128">Macro</span><span class="sxs-lookup"><span data-stu-id="fc105-128">Macro</span></span>                                | <span data-ttu-id="fc105-129">Description</span><span class="sxs-lookup"><span data-stu-id="fc105-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc105-130">**GetBValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="fc105-131">Obtient une valeur bleu RVB.</span><span class="sxs-lookup"><span data-stu-id="fc105-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="fc105-132">**GetGValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="fc105-133">Obtient une valeur vert RVB.</span><span class="sxs-lookup"><span data-stu-id="fc105-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="fc105-134">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="fc105-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="fc105-135">Obtient une valeur rouge RVB.</span><span class="sxs-lookup"><span data-stu-id="fc105-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="fc105-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc105-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="fc105-137">Accepte un index pour une entrée de palette de couleurs logiques et retourne un spécificateur de saisie de palette.</span><span class="sxs-lookup"><span data-stu-id="fc105-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="fc105-138">**PALETTERGB**</span><span class="sxs-lookup"><span data-stu-id="fc105-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="fc105-139">Accepte trois valeurs qui représentent les indizaines relatives de rouge, de vert et de bleu et retourne un spécificateur rouge, vert, bleu (RVB) relatif à la palette.</span><span class="sxs-lookup"><span data-stu-id="fc105-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="fc105-140">RGB</span><span class="sxs-lookup"><span data-stu-id="fc105-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="fc105-141">Sélectionne une couleur rouge, verte, bleue (RVB) en fonction des arguments fournis et des fonctionnalités de couleur du périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="fc105-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 