---
title: Attribut DashStyle de VML
description: Attribut DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315317"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="da16d-103">Attribut DashStyle de VML</span><span class="sxs-lookup"><span data-stu-id="da16d-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="da16d-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="da16d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="da16d-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="da16d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="da16d-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="da16d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="da16d-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="da16d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="da16d-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="da16d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="da16d-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="da16d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="da16d-110">Spécifie le motif de point et de tiret pour un trait.</span><span class="sxs-lookup"><span data-stu-id="da16d-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="da16d-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="da16d-111">Read/write.</span></span> <span data-ttu-id="da16d-112">**VgLineDashStyle**.</span><span class="sxs-lookup"><span data-stu-id="da16d-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="da16d-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="da16d-113">**Applies To**</span></span>

[<span data-ttu-id="da16d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="da16d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="da16d-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="da16d-115">**Tag Syntax**</span></span>

<span data-ttu-id="da16d-116"><v : *Element* DashStyle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="da16d-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="da16d-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="da16d-117">**Script Syntax**</span></span>

<span data-ttu-id="da16d-118">*Element* . DashStyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="da16d-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="da16d-119">*expression* = *Element*. DashStyle</span><span class="sxs-lookup"><span data-stu-id="da16d-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="da16d-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="da16d-120">**Remarks**</span></span>

<span data-ttu-id="da16d-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="da16d-121">Values include:</span></span>

-   <span data-ttu-id="da16d-122">Unie (par défaut)</span><span class="sxs-lookup"><span data-stu-id="da16d-122">Solid (default)</span></span>
-   <span data-ttu-id="da16d-123">ShortDash</span><span class="sxs-lookup"><span data-stu-id="da16d-123">ShortDash</span></span>
-   <span data-ttu-id="da16d-124">ShortDot</span><span class="sxs-lookup"><span data-stu-id="da16d-124">ShortDot</span></span>
-   <span data-ttu-id="da16d-125">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="da16d-125">ShortDashDot</span></span>
-   <span data-ttu-id="da16d-126">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="da16d-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="da16d-127">Points</span><span class="sxs-lookup"><span data-stu-id="da16d-127">Dot</span></span>
-   <span data-ttu-id="da16d-128">Tiret</span><span class="sxs-lookup"><span data-stu-id="da16d-128">Dash</span></span>
-   <span data-ttu-id="da16d-129">LongDash</span><span class="sxs-lookup"><span data-stu-id="da16d-129">LongDash</span></span>
-   <span data-ttu-id="da16d-130">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="da16d-130">DashDot</span></span>
-   <span data-ttu-id="da16d-131">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="da16d-131">LongDashDot</span></span>
-   <span data-ttu-id="da16d-132">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="da16d-132">LongDashDotDot</span></span>

<span data-ttu-id="da16d-133">L’attribut **DashStyle** permet à l’utilisateur de spécifier un modèle de tirets personnalisé.</span><span class="sxs-lookup"><span data-stu-id="da16d-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="da16d-134">Cette opération s’effectue à l’aide d’une série de nombres.</span><span class="sxs-lookup"><span data-stu-id="da16d-134">This is done using a series of numbers.</span></span> <span data-ttu-id="da16d-135">Les styles de tirets sont définis en termes de longueur du tiret (partie dessinée du trait) et de la longueur de l’espace entre les tirets.</span><span class="sxs-lookup"><span data-stu-id="da16d-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="da16d-136">Les longueurs sont exprimées par rapport à la largeur de la ligne : la longueur de « 1 » est égale à la largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="da16d-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="da16d-137">Le style d' **extrémité** est appliqué à chaque tiret, le style de flèche n’est pas.</span><span class="sxs-lookup"><span data-stu-id="da16d-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="da16d-138">La chaîne définit d’abord la longueur du tiret, puis la longueur de l’espace.</span><span class="sxs-lookup"><span data-stu-id="da16d-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="da16d-139">Cela peut être répété pour former des styles de tiret complexes.</span><span class="sxs-lookup"><span data-stu-id="da16d-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="da16d-140">La chaîne doit toujours contenir une paire de nombres ; Si elle contient un nombre impair de nombres, la dernière peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="da16d-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="da16d-141">Le tableau suivant répertorie des valeurs typiques et une description de l’effet prévu.</span><span class="sxs-lookup"><span data-stu-id="da16d-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="da16d-142">« 0 » implique un point qui doit être quatre symétrique (avec des extrémités arrondies, il doit s’agir d’un cercle).</span><span class="sxs-lookup"><span data-stu-id="da16d-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="da16d-143">Si le capuchon de fin de ligne est « plat », une visionneuse doit choisir un tiret de système d’exploitation intégré si possible (en d’autres termes.</span><span class="sxs-lookup"><span data-stu-id="da16d-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="da16d-144">un point rapide à dessiner.</span><span class="sxs-lookup"><span data-stu-id="da16d-144">something that is fast to draw.).</span></span> <span data-ttu-id="da16d-145">Le tableau suivant présente quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="da16d-145">The following table shows some examples.</span></span>



| <span data-ttu-id="da16d-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="da16d-146">DashStyle</span></span>     | <span data-ttu-id="da16d-147">Description</span><span class="sxs-lookup"><span data-stu-id="da16d-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da16d-148">« 2 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-148">"2 2"</span></span>         | <span data-ttu-id="da16d-149">Tirets courts.</span><span class="sxs-lookup"><span data-stu-id="da16d-149">Short-dashes.</span></span> <span data-ttu-id="da16d-150">Chaque tiret et l’espace entre est le double de la largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="da16d-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="da16d-151">« 0 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-151">"0 2"</span></span>         | <span data-ttu-id="da16d-152">Pointillé.</span><span class="sxs-lookup"><span data-stu-id="da16d-152">Dots.</span></span> <span data-ttu-id="da16d-153">L’espace entre est le double de la largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="da16d-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="da16d-154">« 2 2 0 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-154">"2 2 0 2"</span></span>     | <span data-ttu-id="da16d-155">Tiret cadratin-point.</span><span class="sxs-lookup"><span data-stu-id="da16d-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="da16d-156">« 2 2 0 2 0 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="da16d-157">Bref tiret-point-point.</span><span class="sxs-lookup"><span data-stu-id="da16d-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="da16d-158">« 1 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-158">"1 2"</span></span>         | <span data-ttu-id="da16d-159">Cédé.</span><span class="sxs-lookup"><span data-stu-id="da16d-159">Dot.</span></span> <span data-ttu-id="da16d-160">Chaque tiret correspond à la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="da16d-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="da16d-161">« 4 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-161">"4 2"</span></span>         | <span data-ttu-id="da16d-162">Bord.</span><span class="sxs-lookup"><span data-stu-id="da16d-162">Dash.</span></span> <span data-ttu-id="da16d-163">Chaque tiret correspond à quatre fois la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="da16d-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="da16d-164">« 8 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-164">"8 2"</span></span>         | <span data-ttu-id="da16d-165">Long Dash.</span><span class="sxs-lookup"><span data-stu-id="da16d-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="da16d-166">« 4 2 1 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-166">"4 2 1 2"</span></span>     | <span data-ttu-id="da16d-167">Tiret-point.</span><span class="sxs-lookup"><span data-stu-id="da16d-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="da16d-168">« 8 2 1 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-168">"8 2 1 2"</span></span>     | <span data-ttu-id="da16d-169">Long tiret-point.</span><span class="sxs-lookup"><span data-stu-id="da16d-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="da16d-170">« 8 2 1 2 1 2 »</span><span class="sxs-lookup"><span data-stu-id="da16d-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="da16d-171">Long tiret-point-point.</span><span class="sxs-lookup"><span data-stu-id="da16d-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="da16d-172">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="da16d-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="da16d-173">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="da16d-173">**Example**</span></span>

<span data-ttu-id="da16d-174">La forme a un style de tiret d’alternance des tirets et des points.</span><span class="sxs-lookup"><span data-stu-id="da16d-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 