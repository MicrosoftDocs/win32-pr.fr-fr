---
title: Comportement de substitution de la police HTML
description: Comportement de substitution de la police HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106527560"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="ece41-103">Comportement de substitution de la police HTML</span><span class="sxs-lookup"><span data-stu-id="ece41-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="ece41-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="ece41-104">Platform</span></span>

<span data-ttu-id="ece41-105">Clients-\* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ece41-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="ece41-106">**Serveurs-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ece41-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="ece41-107">Description</span><span class="sxs-lookup"><span data-stu-id="ece41-107">Description</span></span>

<span data-ttu-id="ece41-108">Microsoft met à jour la logique des polices de l’interface utilisateur pour plusieurs langues dans les applications du Windows Store en HTML.</span><span class="sxs-lookup"><span data-stu-id="ece41-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="ece41-109">Au lieu d’utiliser une police unique pour toutes les langues, la police de l’interface utilisateur est maintenant déterminée en fonction de la langue.</span><span class="sxs-lookup"><span data-stu-id="ece41-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="ece41-110">Par exemple, les polices de l’interface utilisateur pour le japonais seront désormais Meiryo l’interface utilisateur dans les applications qui utilisent HTML.</span><span class="sxs-lookup"><span data-stu-id="ece41-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ece41-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="ece41-111">Manifestation</span></span>

<span data-ttu-id="ece41-112">Les applications qui dépendent d’une police ancienne peuvent paraître différentes ; Bien que l’apparence de votre application soit améliorée en général grâce à des polices plus lisibles, il peut y avoir un problème avec les dispositions qui dépendent de la taille de contenu parfait.</span><span class="sxs-lookup"><span data-stu-id="ece41-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="ece41-113">Par exemple, certaines lignes de contenu peuvent être plus volumineuses qu’elles ne l’étaient auparavant, provoquant des sauts de ligne et/ou un redimensionnement inattendus des éléments de conteneur.</span><span class="sxs-lookup"><span data-stu-id="ece41-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="ece41-114">Toutefois, dans la pratique, nous n’avons remarqué aucun problème avec les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="ece41-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="ece41-115">Solution</span><span class="sxs-lookup"><span data-stu-id="ece41-115">Solution</span></span>

<span data-ttu-id="ece41-116">Les applications affectées peuvent atténuer ce comportement en spécifiant une police donnée via CSS (par exemple, « font-family : Meiryo UI ») au lieu de compter sur les anciennes polices par défaut.</span><span class="sxs-lookup"><span data-stu-id="ece41-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="ece41-117">Le tableau suivant fournit la police de l’interface utilisateur pour chacun des noms de script.</span><span class="sxs-lookup"><span data-stu-id="ece41-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="ece41-118">Nom du script</span><span class="sxs-lookup"><span data-stu-id="ece41-118">Script Name</span></span>        | <span data-ttu-id="ece41-119">Police de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ece41-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="ece41-120">Arabe</span><span class="sxs-lookup"><span data-stu-id="ece41-120">Arabic</span></span>             | <span data-ttu-id="ece41-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-121">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-122">Arménien</span><span class="sxs-lookup"><span data-stu-id="ece41-122">Armenian</span></span>           | <span data-ttu-id="ece41-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-123">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-124">Bengali</span><span class="sxs-lookup"><span data-stu-id="ece41-124">Bengali</span></span>            | <span data-ttu-id="ece41-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-125">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-126">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="ece41-126">Bopomofo</span></span>           | <span data-ttu-id="ece41-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="ece41-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="ece41-128">Braille</span><span class="sxs-lookup"><span data-stu-id="ece41-128">Braille</span></span>            | <span data-ttu-id="ece41-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-130">Bugi</span><span class="sxs-lookup"><span data-stu-id="ece41-130">Buginese</span></span>           | <span data-ttu-id="ece41-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="ece41-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="ece41-132">SYLLABE CANADIENNE</span><span class="sxs-lookup"><span data-stu-id="ece41-132">Canadian Syllabics</span></span> | <span data-ttu-id="ece41-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="ece41-133">Gadugi</span></span>                |
| <span data-ttu-id="ece41-134">Cherokee</span><span class="sxs-lookup"><span data-stu-id="ece41-134">Cherokee</span></span>           | <span data-ttu-id="ece41-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="ece41-135">Gadugi</span></span>                |
| <span data-ttu-id="ece41-136">Copte</span><span class="sxs-lookup"><span data-stu-id="ece41-136">Coptic</span></span>             | <span data-ttu-id="ece41-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-138">Han (simplifié)</span><span class="sxs-lookup"><span data-stu-id="ece41-138">Han (Simplified)</span></span>   | <span data-ttu-id="ece41-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="ece41-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="ece41-140">Han (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="ece41-140">Han (Traditional)</span></span>  | <span data-ttu-id="ece41-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="ece41-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="ece41-142">Cyrillique</span><span class="sxs-lookup"><span data-stu-id="ece41-142">Cyrillic</span></span>           | <span data-ttu-id="ece41-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-143">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-144">Dévanâgarî</span><span class="sxs-lookup"><span data-stu-id="ece41-144">Devanagari</span></span>         | <span data-ttu-id="ece41-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-145">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-146">Deseret</span><span class="sxs-lookup"><span data-stu-id="ece41-146">Deseret</span></span>            | <span data-ttu-id="ece41-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-148">Éthiopien</span><span class="sxs-lookup"><span data-stu-id="ece41-148">Ethiopic</span></span>           | <span data-ttu-id="ece41-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="ece41-149">Ebrima</span></span>                |
| <span data-ttu-id="ece41-150">Géorgien</span><span class="sxs-lookup"><span data-stu-id="ece41-150">Georgian</span></span>           | <span data-ttu-id="ece41-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-151">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-152">Lettre</span><span class="sxs-lookup"><span data-stu-id="ece41-152">Glagolitic</span></span>         | <span data-ttu-id="ece41-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-154">La</span><span class="sxs-lookup"><span data-stu-id="ece41-154">Gothic</span></span>             | <span data-ttu-id="ece41-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-156">Grec</span><span class="sxs-lookup"><span data-stu-id="ece41-156">Greek</span></span>              | <span data-ttu-id="ece41-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-157">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-158">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="ece41-158">Gujarati</span></span>           | <span data-ttu-id="ece41-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-159">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-160">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="ece41-160">Gurmukhi</span></span>           | <span data-ttu-id="ece41-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-161">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-162">Hébreu</span><span class="sxs-lookup"><span data-stu-id="ece41-162">Hebrew</span></span>             | <span data-ttu-id="ece41-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-163">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-164">Ancien italique</span><span class="sxs-lookup"><span data-stu-id="ece41-164">Old Italic</span></span>         | <span data-ttu-id="ece41-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-166">Javanais</span><span class="sxs-lookup"><span data-stu-id="ece41-166">Javanese</span></span>           | <span data-ttu-id="ece41-167">Texte javanais</span><span class="sxs-lookup"><span data-stu-id="ece41-167">Javanese Text</span></span>         |
| <span data-ttu-id="ece41-168">Japonais</span><span class="sxs-lookup"><span data-stu-id="ece41-168">Japanese</span></span>           | <span data-ttu-id="ece41-169">Interface utilisateur Meiryo</span><span class="sxs-lookup"><span data-stu-id="ece41-169">Meiryo UI</span></span>             |
| <span data-ttu-id="ece41-170">Kannada</span><span class="sxs-lookup"><span data-stu-id="ece41-170">Kannada</span></span>            | <span data-ttu-id="ece41-171">Interface utilisateur Mirmala</span><span class="sxs-lookup"><span data-stu-id="ece41-171">Mirmala UI</span></span>            |
| <span data-ttu-id="ece41-172">Khmer</span><span class="sxs-lookup"><span data-stu-id="ece41-172">Khmer</span></span>              | <span data-ttu-id="ece41-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="ece41-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="ece41-174">Coréen</span><span class="sxs-lookup"><span data-stu-id="ece41-174">Korean</span></span>             | <span data-ttu-id="ece41-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="ece41-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="ece41-176">Lao</span><span class="sxs-lookup"><span data-stu-id="ece41-176">Lao</span></span>                | <span data-ttu-id="ece41-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="ece41-177">Leelawadee</span></span>            |
| <span data-ttu-id="ece41-178">Latin</span><span class="sxs-lookup"><span data-stu-id="ece41-178">Latin</span></span>              | <span data-ttu-id="ece41-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="ece41-179">Segoe UI</span></span>              |
| <span data-ttu-id="ece41-180">Malayalam</span><span class="sxs-lookup"><span data-stu-id="ece41-180">Malayalam</span></span>          | <span data-ttu-id="ece41-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-181">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-182">Mongol</span><span class="sxs-lookup"><span data-stu-id="ece41-182">Mongolian</span></span>          | <span data-ttu-id="ece41-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="ece41-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="ece41-184">Myanmar</span><span class="sxs-lookup"><span data-stu-id="ece41-184">Myanmar</span></span>            | <span data-ttu-id="ece41-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="ece41-185">Myanmar Text</span></span>          |
| <span data-ttu-id="ece41-186">N’ko</span><span class="sxs-lookup"><span data-stu-id="ece41-186">N'Ko</span></span>               | <span data-ttu-id="ece41-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="ece41-187">Ebrima</span></span>                |
| <span data-ttu-id="ece41-188">OGAM</span><span class="sxs-lookup"><span data-stu-id="ece41-188">Ogham</span></span>              | <span data-ttu-id="ece41-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-190">Ol tchiki</span><span class="sxs-lookup"><span data-stu-id="ece41-190">Ol Chiki</span></span>           | <span data-ttu-id="ece41-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-191">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-192">Ancien turc</span><span class="sxs-lookup"><span data-stu-id="ece41-192">Old Turkic</span></span>         | <span data-ttu-id="ece41-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-194">Odia</span><span class="sxs-lookup"><span data-stu-id="ece41-194">Oriya</span></span>              | <span data-ttu-id="ece41-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-195">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-196">Osmanya</span><span class="sxs-lookup"><span data-stu-id="ece41-196">Osmanya</span></span>            | <span data-ttu-id="ece41-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="ece41-197">Ebrima</span></span>                |
| <span data-ttu-id="ece41-198">PHAGS-PA</span><span class="sxs-lookup"><span data-stu-id="ece41-198">Phags-pa</span></span>           | <span data-ttu-id="ece41-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="ece41-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="ece41-200">Lettre</span><span class="sxs-lookup"><span data-stu-id="ece41-200">Runic</span></span>              | <span data-ttu-id="ece41-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="ece41-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="ece41-202">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="ece41-202">Sora Sompeng</span></span>       | <span data-ttu-id="ece41-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-203">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-204">Cingalais</span><span class="sxs-lookup"><span data-stu-id="ece41-204">Sinhala</span></span>            | <span data-ttu-id="ece41-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-205">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-206">Syriaque</span><span class="sxs-lookup"><span data-stu-id="ece41-206">Syriac</span></span>             | <span data-ttu-id="ece41-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="ece41-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="ece41-208">LETTRE TAÏ le</span><span class="sxs-lookup"><span data-stu-id="ece41-208">Tai Le</span></span>             | <span data-ttu-id="ece41-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="ece41-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="ece41-210">Nouveau taï lü</span><span class="sxs-lookup"><span data-stu-id="ece41-210">New Tai Lue</span></span>        | <span data-ttu-id="ece41-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="ece41-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="ece41-212">Tamoul</span><span class="sxs-lookup"><span data-stu-id="ece41-212">Tamil</span></span>              | <span data-ttu-id="ece41-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-213">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-214">Télougou</span><span class="sxs-lookup"><span data-stu-id="ece41-214">Telugu</span></span>             | <span data-ttu-id="ece41-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="ece41-215">Nirmala UI</span></span>            |
| <span data-ttu-id="ece41-216">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="ece41-216">Tifinagh</span></span>           | <span data-ttu-id="ece41-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="ece41-217">Ebrima</span></span>                |
| <span data-ttu-id="ece41-218">Tana</span><span class="sxs-lookup"><span data-stu-id="ece41-218">Thaana</span></span>             | <span data-ttu-id="ece41-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="ece41-219">MV Boli</span></span>               |
| <span data-ttu-id="ece41-220">Thaï</span><span class="sxs-lookup"><span data-stu-id="ece41-220">Thai</span></span>               | <span data-ttu-id="ece41-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="ece41-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="ece41-222">Tibétain</span><span class="sxs-lookup"><span data-stu-id="ece41-222">Tibetan</span></span>            | <span data-ttu-id="ece41-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="ece41-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="ece41-224">Vaï</span><span class="sxs-lookup"><span data-stu-id="ece41-224">Vai</span></span>                | <span data-ttu-id="ece41-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="ece41-225">Ebrima</span></span>                |
| <span data-ttu-id="ece41-226">Yi</span><span class="sxs-lookup"><span data-stu-id="ece41-226">Yi</span></span>                 | <span data-ttu-id="ece41-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="ece41-227">Microsoft Yi Baiti</span></span>    |



 

 

 




