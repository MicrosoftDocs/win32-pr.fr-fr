---
title: Mappage des flux RSS sur les propriétés de Gestionnaire de périphériques Windows Media
description: Mappage des flux RSS sur les propriétés de Gestionnaire de périphériques Windows Media
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Gestionnaire de périphériques Windows Media, flux RSS
- Gestionnaire de périphériques, flux RSS
- Guide de programmation, flux RSS
- applications de bureau, flux RSS
- création d’applications Windows Media Gestionnaire de périphériques, flux RSS
- Flux RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839457"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="7717b-109">Mappage des flux RSS sur les propriétés de Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="7717b-110">Le lecteur Windows Media 11 fournit une fonctionnalité d’agrégation RSS qui permet aux utilisateurs de stocker du contenu obtenu à partir de podcasts sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7717b-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="7717b-111">Cette rubrique décrit les éléments XML trouvés dans un flux RSS.</span><span class="sxs-lookup"><span data-stu-id="7717b-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="7717b-112">En outre, il mappe ces éléments RSS aux propriétés de Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7717b-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="7717b-113">Les éléments d’un flux RSS possèdent la hiérarchie et les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="7717b-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="7717b-114">Le tableau suivant répertorie les éléments de canal dans un flux RSS et les propriétés Windows Media Gestionnaire de périphériques correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7717b-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="7717b-115">Élément Channel</span><span class="sxs-lookup"><span data-stu-id="7717b-115">Channel element</span></span> | <span data-ttu-id="7717b-116">Statut</span><span class="sxs-lookup"><span data-stu-id="7717b-116">Status</span></span>         | <span data-ttu-id="7717b-117">Propriété Windows Media Gestionnaire de périphériques correspondante</span><span class="sxs-lookup"><span data-stu-id="7717b-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="7717b-118">catégorie</span><span class="sxs-lookup"><span data-stu-id="7717b-118">category</span></span>        | <span data-ttu-id="7717b-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-119">Optional</span></span>       | [<span data-ttu-id="7717b-120">\_wszWMDMGenre g</span><span class="sxs-lookup"><span data-stu-id="7717b-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="7717b-121">cloud</span><span class="sxs-lookup"><span data-stu-id="7717b-121">cloud</span></span>           | <span data-ttu-id="7717b-122">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-122">Not applicable</span></span> | <span data-ttu-id="7717b-123">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-123">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-124">copyright</span><span class="sxs-lookup"><span data-stu-id="7717b-124">copyright</span></span>       | <span data-ttu-id="7717b-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-125">Optional</span></span>       | [<span data-ttu-id="7717b-126">\_wszWMDMProviderCopyright g</span><span class="sxs-lookup"><span data-stu-id="7717b-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="7717b-127">description</span><span class="sxs-lookup"><span data-stu-id="7717b-127">description</span></span>     | <span data-ttu-id="7717b-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-128">Required</span></span>       | [<span data-ttu-id="7717b-129">\_wszWMDMDescription g</span><span class="sxs-lookup"><span data-stu-id="7717b-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="7717b-130">docs</span><span class="sxs-lookup"><span data-stu-id="7717b-130">docs</span></span>            | <span data-ttu-id="7717b-131">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-131">Not applicable</span></span> | <span data-ttu-id="7717b-132">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-132">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-133">générateur</span><span class="sxs-lookup"><span data-stu-id="7717b-133">generator</span></span>       | <span data-ttu-id="7717b-134">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-134">Not applicable</span></span> | <span data-ttu-id="7717b-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-135">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-136">langage</span><span class="sxs-lookup"><span data-stu-id="7717b-136">language</span></span>        | <span data-ttu-id="7717b-137">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-137">Not applicable</span></span> | <span data-ttu-id="7717b-138">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-138">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="7717b-139">lastBuildDate</span></span>   | <span data-ttu-id="7717b-140">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-140">Optional</span></span>       | [<span data-ttu-id="7717b-141">\_wszWMDMLastModifiedDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="7717b-142">link</span><span class="sxs-lookup"><span data-stu-id="7717b-142">link</span></span>            | <span data-ttu-id="7717b-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-143">Required</span></span>       | [<span data-ttu-id="7717b-144">\_wszWMDMDestinationURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="7717b-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="7717b-145">managingEditor</span></span>  | <span data-ttu-id="7717b-146">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-146">Optional</span></span>       | [<span data-ttu-id="7717b-147">\_wszWMDMEditor g</span><span class="sxs-lookup"><span data-stu-id="7717b-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="7717b-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="7717b-148">pubDate</span></span>         | <span data-ttu-id="7717b-149">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-149">Optional</span></span>       | [<span data-ttu-id="7717b-150">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="7717b-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="7717b-151">rating</span><span class="sxs-lookup"><span data-stu-id="7717b-151">rating</span></span>          | <span data-ttu-id="7717b-152">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-152">Not applicable</span></span> | <span data-ttu-id="7717b-153">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-153">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-154">skipDays</span><span class="sxs-lookup"><span data-stu-id="7717b-154">skipDays</span></span>        | <span data-ttu-id="7717b-155">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-155">Not applicable</span></span> | <span data-ttu-id="7717b-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-156">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-157">skipHours</span><span class="sxs-lookup"><span data-stu-id="7717b-157">skipHours</span></span>       | <span data-ttu-id="7717b-158">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-158">Not applicable</span></span> | <span data-ttu-id="7717b-159">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-159">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-160">textInput</span><span class="sxs-lookup"><span data-stu-id="7717b-160">textInput</span></span>       | <span data-ttu-id="7717b-161">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-161">Not applicable</span></span> | <span data-ttu-id="7717b-162">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-162">Not applicable</span></span>                                        |
| <span data-ttu-id="7717b-163">title</span><span class="sxs-lookup"><span data-stu-id="7717b-163">title</span></span>           | <span data-ttu-id="7717b-164">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-164">Required</span></span>       | [<span data-ttu-id="7717b-165">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="7717b-166">ttl</span><span class="sxs-lookup"><span data-stu-id="7717b-166">ttl</span></span>             | <span data-ttu-id="7717b-167">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-167">Optional</span></span>       | [<span data-ttu-id="7717b-168">\_wszWMDMTimeToLive g</span><span class="sxs-lookup"><span data-stu-id="7717b-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="7717b-169">webMaster</span><span class="sxs-lookup"><span data-stu-id="7717b-169">webMaster</span></span>       | <span data-ttu-id="7717b-170">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-170">Optional</span></span>       | [<span data-ttu-id="7717b-171">\_wszWMDMWebMaster g</span><span class="sxs-lookup"><span data-stu-id="7717b-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="7717b-172">Le tableau suivant répertorie les éléments d’image dans un flux RSS et les propriétés WMDM correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7717b-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="7717b-173">Élément Image</span><span class="sxs-lookup"><span data-stu-id="7717b-173">Image element</span></span> | <span data-ttu-id="7717b-174">Statut</span><span class="sxs-lookup"><span data-stu-id="7717b-174">Status</span></span>   | <span data-ttu-id="7717b-175">Propriété Windows Media Gestionnaire de périphériques correspondante</span><span class="sxs-lookup"><span data-stu-id="7717b-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="7717b-176">description</span><span class="sxs-lookup"><span data-stu-id="7717b-176">description</span></span>   | <span data-ttu-id="7717b-177">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-177">Optional</span></span> | [<span data-ttu-id="7717b-178">\_wszWMDMDescription g</span><span class="sxs-lookup"><span data-stu-id="7717b-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="7717b-179">height</span><span class="sxs-lookup"><span data-stu-id="7717b-179">height</span></span>        | <span data-ttu-id="7717b-180">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-180">Optional</span></span> | [<span data-ttu-id="7717b-181">\_wszWMDMHeight g</span><span class="sxs-lookup"><span data-stu-id="7717b-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="7717b-182">link</span><span class="sxs-lookup"><span data-stu-id="7717b-182">link</span></span>          | <span data-ttu-id="7717b-183">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-183">Optional</span></span> | [<span data-ttu-id="7717b-184">\_wszWMDMDestinationURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="7717b-185">title</span><span class="sxs-lookup"><span data-stu-id="7717b-185">title</span></span>         | <span data-ttu-id="7717b-186">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-186">Optional</span></span> | [<span data-ttu-id="7717b-187">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="7717b-188">url</span><span class="sxs-lookup"><span data-stu-id="7717b-188">url</span></span>           | <span data-ttu-id="7717b-189">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-189">Optional</span></span> | [<span data-ttu-id="7717b-190">\_wszWMDMSourceURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="7717b-191">width</span><span class="sxs-lookup"><span data-stu-id="7717b-191">width</span></span>         | <span data-ttu-id="7717b-192">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-192">Optional</span></span> | [<span data-ttu-id="7717b-193">\_wszWMDMWidth g</span><span class="sxs-lookup"><span data-stu-id="7717b-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="7717b-194">Le tableau suivant répertorie les éléments Item d’un flux RSS et les propriétés Windows Media Gestionnaire de périphériques correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7717b-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="7717b-195">Item, élément</span><span class="sxs-lookup"><span data-stu-id="7717b-195">Item element</span></span> | <span data-ttu-id="7717b-196">Attribut</span><span class="sxs-lookup"><span data-stu-id="7717b-196">Attribute</span></span>   | <span data-ttu-id="7717b-197">Statut</span><span class="sxs-lookup"><span data-stu-id="7717b-197">Status</span></span>         | <span data-ttu-id="7717b-198">Propriété Windows Media Gestionnaire de périphériques correspondante</span><span class="sxs-lookup"><span data-stu-id="7717b-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="7717b-199">auteur</span><span class="sxs-lookup"><span data-stu-id="7717b-199">author</span></span>       |             | <span data-ttu-id="7717b-200">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-200">Optional</span></span>       | [<span data-ttu-id="7717b-201">\_wszWMDMAuthor g</span><span class="sxs-lookup"><span data-stu-id="7717b-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="7717b-202">catégorie</span><span class="sxs-lookup"><span data-stu-id="7717b-202">category</span></span>     |             | <span data-ttu-id="7717b-203">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-203">Optional</span></span>       | [<span data-ttu-id="7717b-204">\_wszWMDMGenre g</span><span class="sxs-lookup"><span data-stu-id="7717b-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="7717b-205">domaine</span><span class="sxs-lookup"><span data-stu-id="7717b-205">domain</span></span>      | <span data-ttu-id="7717b-206">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-206">Not applicable</span></span> | <span data-ttu-id="7717b-207">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="7717b-208">description</span><span class="sxs-lookup"><span data-stu-id="7717b-208">description</span></span>  |             | <span data-ttu-id="7717b-209">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-209">Optional</span></span>       | [<span data-ttu-id="7717b-210">\_wszWMDMDescription g</span><span class="sxs-lookup"><span data-stu-id="7717b-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="7717b-211">coffret</span><span class="sxs-lookup"><span data-stu-id="7717b-211">enclosure</span></span>    |             | <span data-ttu-id="7717b-212">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-212">Optional</span></span>       | <span data-ttu-id="7717b-213">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="7717b-214">length</span><span class="sxs-lookup"><span data-stu-id="7717b-214">length</span></span>      | <span data-ttu-id="7717b-215">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-215">Required</span></span>       | [<span data-ttu-id="7717b-216">\_wszWMDMFileSize g</span><span class="sxs-lookup"><span data-stu-id="7717b-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="7717b-217">type</span><span class="sxs-lookup"><span data-stu-id="7717b-217">type</span></span>        | <span data-ttu-id="7717b-218">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-218">Required</span></span>       | <span data-ttu-id="7717b-219">(Le type MIME doit être mappé au type de contenu de la propriété.)</span><span class="sxs-lookup"><span data-stu-id="7717b-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="7717b-220">url</span><span class="sxs-lookup"><span data-stu-id="7717b-220">url</span></span>         | <span data-ttu-id="7717b-221">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7717b-221">Required</span></span>       | [<span data-ttu-id="7717b-222">\_wszWMDMSourceURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="7717b-223">guid</span><span class="sxs-lookup"><span data-stu-id="7717b-223">guid</span></span>         |             | <span data-ttu-id="7717b-224">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-224">Optional</span></span>       | [<span data-ttu-id="7717b-225">\_wszWMDMediaGuid g</span><span class="sxs-lookup"><span data-stu-id="7717b-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="7717b-226">isPermaLink</span><span class="sxs-lookup"><span data-stu-id="7717b-226">isPermaLink</span></span> | <span data-ttu-id="7717b-227">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-227">Not applicable</span></span> | <span data-ttu-id="7717b-228">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="7717b-229">link</span><span class="sxs-lookup"><span data-stu-id="7717b-229">link</span></span>         |             | <span data-ttu-id="7717b-230">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-230">Optional</span></span>       | [<span data-ttu-id="7717b-231">\_wszWMDMDestinationURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="7717b-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="7717b-232">pubDate</span></span>      |             | <span data-ttu-id="7717b-233">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-233">Optional</span></span>       | [<span data-ttu-id="7717b-234">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="7717b-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="7717b-235">source</span><span class="sxs-lookup"><span data-stu-id="7717b-235">source</span></span>       |             | <span data-ttu-id="7717b-236">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-236">Not applicable</span></span> | <span data-ttu-id="7717b-237">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7717b-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="7717b-238">title</span><span class="sxs-lookup"><span data-stu-id="7717b-238">title</span></span>        |             | <span data-ttu-id="7717b-239">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7717b-239">Optional</span></span>       | [<span data-ttu-id="7717b-240">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="7717b-241">Exemple</span><span class="sxs-lookup"><span data-stu-id="7717b-241">Example</span></span>

<span data-ttu-id="7717b-242">L’exemple suivant montre un flux RSS complet pour un podcast fictif fourni par le PDG d’une société de publication.</span><span class="sxs-lookup"><span data-stu-id="7717b-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="7717b-243">Mappage d’éléments de canal RSS avec les valeurs de Propriété Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="7717b-244">Le tableau suivant décrit comment les valeurs des éléments de canal RSS de l’exemple précédent sont mappées à des propriétés de Gestionnaire de périphériques Windows Media particulières.</span><span class="sxs-lookup"><span data-stu-id="7717b-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="7717b-245">Propriété de Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="7717b-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="7717b-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7717b-247">\_wszWMDMAuthorDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="7717b-248">Vendredi 9 juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="7717b-249">\_wszWMDMDESCRIPTION g</span><span class="sxs-lookup"><span data-stu-id="7717b-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="7717b-250">Peter Bankov, PDG de Lucerne Publishing, examine les dernières tendances des publications en ligne.</span><span class="sxs-lookup"><span data-stu-id="7717b-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="7717b-251">\_URL wszWMDMDESTINATION \_ g</span><span class="sxs-lookup"><span data-stu-id="7717b-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="7717b-252">\_wszWMDMEDITOR g</span><span class="sxs-lookup"><span data-stu-id="7717b-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="7717b-253">\_wszWMDMFileCreationDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="7717b-254">Vendredi 9 juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="7717b-255">\_wszWMDMFileName g</span><span class="sxs-lookup"><span data-stu-id="7717b-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="7717b-256">La publication numérique</span><span class="sxs-lookup"><span data-stu-id="7717b-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="7717b-257">\_wszWMDMFileSize g</span><span class="sxs-lookup"><span data-stu-id="7717b-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="7717b-258">13 790</span><span class="sxs-lookup"><span data-stu-id="7717b-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="7717b-259">\_wszWMDMFormatCode g</span><span class="sxs-lookup"><span data-stu-id="7717b-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="7717b-260">WMDM \_ FORMATCODE \_ Media \_ cast</span><span class="sxs-lookup"><span data-stu-id="7717b-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="7717b-261">\_wszWMDMGENRE g</span><span class="sxs-lookup"><span data-stu-id="7717b-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="7717b-262">Actualités</span><span class="sxs-lookup"><span data-stu-id="7717b-262">News</span></span>                                                                                          |
| [<span data-ttu-id="7717b-263">\_wszWMDMLAST \_ Date de modification \_ du g</span><span class="sxs-lookup"><span data-stu-id="7717b-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="7717b-264">Vendredi 9 juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="7717b-265">\_wszWMDMLastModifiedDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="7717b-266">Vendredi 9 juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="7717b-267">\_wszWMDMProviderCopyright g</span><span class="sxs-lookup"><span data-stu-id="7717b-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="7717b-268">2006 Lucerne Publishing LP, LLLP.</span><span class="sxs-lookup"><span data-stu-id="7717b-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="7717b-269">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="7717b-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="7717b-270">\_wszWMDMTimeToLive g</span><span class="sxs-lookup"><span data-stu-id="7717b-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="7717b-271">240</span><span class="sxs-lookup"><span data-stu-id="7717b-271">240</span></span>                                                                                           |
| [<span data-ttu-id="7717b-272">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="7717b-273">La publication numérique</span><span class="sxs-lookup"><span data-stu-id="7717b-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="7717b-274">\_wszWMDMWEBMASTER g</span><span class="sxs-lookup"><span data-stu-id="7717b-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="7717b-275">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="7717b-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="7717b-276">Vendredi 9 juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="7717b-277">Mappage d’éléments d’image RSS avec les valeurs de Propriété Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="7717b-278">Le tableau suivant décrit comment les valeurs des éléments d’image RSS de l’exemple précédent sont mappées à des propriétés de Gestionnaire de périphériques Windows Media particulières.</span><span class="sxs-lookup"><span data-stu-id="7717b-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="7717b-279">Propriété de Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="7717b-280">Valeur</span><span class="sxs-lookup"><span data-stu-id="7717b-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="7717b-281">\_wszWMDMAlbumCoverFormat g</span><span class="sxs-lookup"><span data-stu-id="7717b-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="7717b-282">\_ \_ gif format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7717b-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="7717b-283">\_wszWMDMAlbumCoverSize g</span><span class="sxs-lookup"><span data-stu-id="7717b-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="7717b-284">512</span><span class="sxs-lookup"><span data-stu-id="7717b-284">512</span></span>                                              |
| [<span data-ttu-id="7717b-285">\_wszWMDMDescription g</span><span class="sxs-lookup"><span data-stu-id="7717b-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="7717b-286">Logo Lucerne</span><span class="sxs-lookup"><span data-stu-id="7717b-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="7717b-287">\_wszWMDMDestinationURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="7717b-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="7717b-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="7717b-289">\_wszWMDMHeight g</span><span class="sxs-lookup"><span data-stu-id="7717b-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="7717b-290">300</span><span class="sxs-lookup"><span data-stu-id="7717b-290">300</span></span>                                              |
| [<span data-ttu-id="7717b-291">\_wszWMDMSourceURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="7717b-292">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="7717b-293">Lucerne Publishing</span><span class="sxs-lookup"><span data-stu-id="7717b-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="7717b-294">\_wszWMDMWidth g</span><span class="sxs-lookup"><span data-stu-id="7717b-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="7717b-295">300</span><span class="sxs-lookup"><span data-stu-id="7717b-295">300</span></span>                                              |



 

<span data-ttu-id="7717b-296">Mappage d’éléments d’élément RSS à des valeurs de Propriété Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="7717b-297">Le tableau suivant décrit comment les valeurs des éléments de l’élément RSS de l’exemple précédent sont mappées à des propriétés Gestionnaire de périphériques Windows Media spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7717b-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="7717b-298">Propriété de Gestionnaire de périphériques Windows Media</span><span class="sxs-lookup"><span data-stu-id="7717b-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="7717b-299">Valeur</span><span class="sxs-lookup"><span data-stu-id="7717b-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7717b-300">\_wszWMDMAuthor g</span><span class="sxs-lookup"><span data-stu-id="7717b-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="7717b-301">Lucerne</span><span class="sxs-lookup"><span data-stu-id="7717b-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="7717b-302">\_wszWMDMAuthorDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="7717b-303">Case, 1er juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="7717b-304">\_wszWMDMDescription g</span><span class="sxs-lookup"><span data-stu-id="7717b-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="7717b-305">Les publications en ligne évoluent rapidement.</span><span class="sxs-lookup"><span data-stu-id="7717b-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="7717b-306">Le PDG d’une maison de publication examine les tendances des cinq dernières années et leurs implications.</span><span class="sxs-lookup"><span data-stu-id="7717b-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="7717b-307">\_wszWMDMDestinationURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="7717b-308">\_wszWMDMDuration g</span><span class="sxs-lookup"><span data-stu-id="7717b-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="7717b-309">120325445</span><span class="sxs-lookup"><span data-stu-id="7717b-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="7717b-310">\_wszWMDMFileCreationDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="7717b-311">Case, 1er juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="7717b-312">\_wszWMDMFileSize g</span><span class="sxs-lookup"><span data-stu-id="7717b-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="7717b-313">10329011</span><span class="sxs-lookup"><span data-stu-id="7717b-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="7717b-314">\_wszWMDMFormatCode g</span><span class="sxs-lookup"><span data-stu-id="7717b-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="7717b-315">\_Mp3 WMDM FORMATCODE \_</span><span class="sxs-lookup"><span data-stu-id="7717b-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="7717b-316">\_wszWMDMGenre g</span><span class="sxs-lookup"><span data-stu-id="7717b-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="7717b-317">Actualités</span><span class="sxs-lookup"><span data-stu-id="7717b-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="7717b-318">\_wszWMDMLastModifiedDate g</span><span class="sxs-lookup"><span data-stu-id="7717b-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="7717b-319">Case, 1er juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="7717b-320">\_wszWMDMMediaGuid g</span><span class="sxs-lookup"><span data-stu-id="7717b-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="7717b-321">\_wszWMDMSourceURL g</span><span class="sxs-lookup"><span data-stu-id="7717b-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="7717b-322">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="7717b-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="7717b-323">La publication numérique</span><span class="sxs-lookup"><span data-stu-id="7717b-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="7717b-324">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="7717b-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="7717b-325">Case, 1er juin 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="7717b-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="7717b-326">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7717b-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7717b-327">**Constantes de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="7717b-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




