---
title: VarFileInfo bloc (instruction)
description: Décrit la forme du bloc d’informations sur les variables.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menus de l’instruction de bloc VarFileInfo et autres ressources
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030384"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="00e67-104">VarFileInfo bloc (instruction)</span><span class="sxs-lookup"><span data-stu-id="00e67-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="00e67-105">Définit un bloc d’informations de variable.</span><span class="sxs-lookup"><span data-stu-id="00e67-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="00e67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00e67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e67-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="00e67-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="00e67-108">Un des identificateurs de langue spécifiés dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="00e67-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="00e67-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="00e67-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="00e67-110">Un des identificateurs de jeu de caractères spécifiés dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="00e67-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00e67-111">Notes</span><span class="sxs-lookup"><span data-stu-id="00e67-111">Remarks</span></span>

<span data-ttu-id="00e67-112">Plusieurs paires d’identificateurs peuvent être fournies, mais chaque paire doit être séparée de la paire précédente par une virgule.</span><span class="sxs-lookup"><span data-stu-id="00e67-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="00e67-113">Le paramètre *LangID* spécifie l’un des codes de langue suivants.</span><span class="sxs-lookup"><span data-stu-id="00e67-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="00e67-114">Code</span><span class="sxs-lookup"><span data-stu-id="00e67-114">Code</span></span>   | <span data-ttu-id="00e67-115">Langage</span><span class="sxs-lookup"><span data-stu-id="00e67-115">Language</span></span>            | <span data-ttu-id="00e67-116">Code</span><span class="sxs-lookup"><span data-stu-id="00e67-116">Code</span></span>   | <span data-ttu-id="00e67-117">Langage</span><span class="sxs-lookup"><span data-stu-id="00e67-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="00e67-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="00e67-118">0x0401</span></span> | <span data-ttu-id="00e67-119">Arabe</span><span class="sxs-lookup"><span data-stu-id="00e67-119">Arabic</span></span>              | <span data-ttu-id="00e67-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="00e67-120">0x0415</span></span> | <span data-ttu-id="00e67-121">Polonais</span><span class="sxs-lookup"><span data-stu-id="00e67-121">Polish</span></span>                    |
| <span data-ttu-id="00e67-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="00e67-122">0x0402</span></span> | <span data-ttu-id="00e67-123">Bulgare</span><span class="sxs-lookup"><span data-stu-id="00e67-123">Bulgarian</span></span>           | <span data-ttu-id="00e67-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="00e67-124">0x0416</span></span> | <span data-ttu-id="00e67-125">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="00e67-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="00e67-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="00e67-126">0x0403</span></span> | <span data-ttu-id="00e67-127">Catalan</span><span class="sxs-lookup"><span data-stu-id="00e67-127">Catalan</span></span>             | <span data-ttu-id="00e67-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="00e67-128">0x0417</span></span> | <span data-ttu-id="00e67-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="00e67-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="00e67-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="00e67-130">0x0404</span></span> | <span data-ttu-id="00e67-131">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="00e67-131">Traditional Chinese</span></span> | <span data-ttu-id="00e67-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="00e67-132">0x0418</span></span> | <span data-ttu-id="00e67-133">Roumain</span><span class="sxs-lookup"><span data-stu-id="00e67-133">Romanian</span></span>                  |
| <span data-ttu-id="00e67-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="00e67-134">0x0405</span></span> | <span data-ttu-id="00e67-135">Tchèque</span><span class="sxs-lookup"><span data-stu-id="00e67-135">Czech</span></span>               | <span data-ttu-id="00e67-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="00e67-136">0x0419</span></span> | <span data-ttu-id="00e67-137">Russe</span><span class="sxs-lookup"><span data-stu-id="00e67-137">Russian</span></span>                   |
| <span data-ttu-id="00e67-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="00e67-138">0x0406</span></span> | <span data-ttu-id="00e67-139">Danois</span><span class="sxs-lookup"><span data-stu-id="00e67-139">Danish</span></span>              | <span data-ttu-id="00e67-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="00e67-140">0x041A</span></span> | <span data-ttu-id="00e67-141">Croato-Serbian (latin)</span><span class="sxs-lookup"><span data-stu-id="00e67-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="00e67-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="00e67-142">0x0407</span></span> | <span data-ttu-id="00e67-143">Allemand</span><span class="sxs-lookup"><span data-stu-id="00e67-143">German</span></span>              | <span data-ttu-id="00e67-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="00e67-144">0x041B</span></span> | <span data-ttu-id="00e67-145">Slovaque</span><span class="sxs-lookup"><span data-stu-id="00e67-145">Slovak</span></span>                    |
| <span data-ttu-id="00e67-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="00e67-146">0x0408</span></span> | <span data-ttu-id="00e67-147">Grec</span><span class="sxs-lookup"><span data-stu-id="00e67-147">Greek</span></span>               | <span data-ttu-id="00e67-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="00e67-148">0x041C</span></span> | <span data-ttu-id="00e67-149">Albanais</span><span class="sxs-lookup"><span data-stu-id="00e67-149">Albanian</span></span>                  |
| <span data-ttu-id="00e67-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="00e67-150">0x0409</span></span> | <span data-ttu-id="00e67-151">Anglais (États-Unis)</span><span class="sxs-lookup"><span data-stu-id="00e67-151">U.S. English</span></span>        | <span data-ttu-id="00e67-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="00e67-152">0x041D</span></span> | <span data-ttu-id="00e67-153">Suédois</span><span class="sxs-lookup"><span data-stu-id="00e67-153">Swedish</span></span>                   |
| <span data-ttu-id="00e67-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="00e67-154">0x040A</span></span> | <span data-ttu-id="00e67-155">Espagnol castillan</span><span class="sxs-lookup"><span data-stu-id="00e67-155">Castilian Spanish</span></span>   | <span data-ttu-id="00e67-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="00e67-156">0x041E</span></span> | <span data-ttu-id="00e67-157">Thaï</span><span class="sxs-lookup"><span data-stu-id="00e67-157">Thai</span></span>                      |
| <span data-ttu-id="00e67-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="00e67-158">0x040B</span></span> | <span data-ttu-id="00e67-159">Finnois</span><span class="sxs-lookup"><span data-stu-id="00e67-159">Finnish</span></span>             | <span data-ttu-id="00e67-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="00e67-160">0x041F</span></span> | <span data-ttu-id="00e67-161">Turc</span><span class="sxs-lookup"><span data-stu-id="00e67-161">Turkish</span></span>                   |
| <span data-ttu-id="00e67-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="00e67-162">0x040C</span></span> | <span data-ttu-id="00e67-163">Français</span><span class="sxs-lookup"><span data-stu-id="00e67-163">French</span></span>              | <span data-ttu-id="00e67-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="00e67-164">0x0420</span></span> | <span data-ttu-id="00e67-165">Ourdou</span><span class="sxs-lookup"><span data-stu-id="00e67-165">Urdu</span></span>                      |
| <span data-ttu-id="00e67-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="00e67-166">0x040D</span></span> | <span data-ttu-id="00e67-167">Hébreu</span><span class="sxs-lookup"><span data-stu-id="00e67-167">Hebrew</span></span>              | <span data-ttu-id="00e67-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="00e67-168">0x0421</span></span> | <span data-ttu-id="00e67-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="00e67-169">Bahasa</span></span>                    |
| <span data-ttu-id="00e67-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="00e67-170">0x040E</span></span> | <span data-ttu-id="00e67-171">Hongrois</span><span class="sxs-lookup"><span data-stu-id="00e67-171">Hungarian</span></span>           | <span data-ttu-id="00e67-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="00e67-172">0x0804</span></span> | <span data-ttu-id="00e67-173">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="00e67-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="00e67-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="00e67-174">0x040F</span></span> | <span data-ttu-id="00e67-175">Islandais</span><span class="sxs-lookup"><span data-stu-id="00e67-175">Icelandic</span></span>           | <span data-ttu-id="00e67-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="00e67-176">0x0807</span></span> | <span data-ttu-id="00e67-177">Allemand Suisse</span><span class="sxs-lookup"><span data-stu-id="00e67-177">Swiss German</span></span>              |
| <span data-ttu-id="00e67-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="00e67-178">0x0410</span></span> | <span data-ttu-id="00e67-179">Italien</span><span class="sxs-lookup"><span data-stu-id="00e67-179">Italian</span></span>             | <span data-ttu-id="00e67-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="00e67-180">0x0809</span></span> | <span data-ttu-id="00e67-181">au Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="00e67-181">U.K.</span></span> <span data-ttu-id="00e67-182">Anglais</span><span class="sxs-lookup"><span data-stu-id="00e67-182">English</span></span>              |
| <span data-ttu-id="00e67-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="00e67-183">0x0411</span></span> | <span data-ttu-id="00e67-184">Japonais</span><span class="sxs-lookup"><span data-stu-id="00e67-184">Japanese</span></span>            | <span data-ttu-id="00e67-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="00e67-185">0x080A</span></span> | <span data-ttu-id="00e67-186">Espagnol (Mexique)</span><span class="sxs-lookup"><span data-stu-id="00e67-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="00e67-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="00e67-187">0x0412</span></span> | <span data-ttu-id="00e67-188">Coréen</span><span class="sxs-lookup"><span data-stu-id="00e67-188">Korean</span></span>              | <span data-ttu-id="00e67-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="00e67-189">0x080C</span></span> | <span data-ttu-id="00e67-190">Français belge</span><span class="sxs-lookup"><span data-stu-id="00e67-190">Belgian French</span></span>            |
| <span data-ttu-id="00e67-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="00e67-191">0x0413</span></span> | <span data-ttu-id="00e67-192">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="00e67-192">Dutch</span></span>               | <span data-ttu-id="00e67-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="00e67-193">0x0C0C</span></span> | <span data-ttu-id="00e67-194">Français (Canada)</span><span class="sxs-lookup"><span data-stu-id="00e67-194">Canadian French</span></span>           |
| <span data-ttu-id="00e67-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="00e67-195">0x0414</span></span> | <span data-ttu-id="00e67-196">Norvégien – bokmal</span><span class="sxs-lookup"><span data-stu-id="00e67-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="00e67-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="00e67-197">0x100C</span></span> | <span data-ttu-id="00e67-198">Français Suisse</span><span class="sxs-lookup"><span data-stu-id="00e67-198">Swiss French</span></span>              |
| <span data-ttu-id="00e67-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="00e67-199">0x0810</span></span> | <span data-ttu-id="00e67-200">Italien Suisse</span><span class="sxs-lookup"><span data-stu-id="00e67-200">Swiss Italian</span></span>       | <span data-ttu-id="00e67-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="00e67-201">0x0816</span></span> | <span data-ttu-id="00e67-202">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="00e67-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="00e67-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="00e67-203">0x0813</span></span> | <span data-ttu-id="00e67-204">Néerlandais (Belgique)</span><span class="sxs-lookup"><span data-stu-id="00e67-204">Belgian Dutch</span></span>       | <span data-ttu-id="00e67-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="00e67-205">0x081A</span></span> | <span data-ttu-id="00e67-206">Serbo-Croatian (cyrillique)</span><span class="sxs-lookup"><span data-stu-id="00e67-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="00e67-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="00e67-207">0x0814</span></span> | <span data-ttu-id="00e67-208">Norvégien – nynorsk</span><span class="sxs-lookup"><span data-stu-id="00e67-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="00e67-209">?</span><span class="sxs-lookup"><span data-stu-id="00e67-209">?</span></span>      | <span data-ttu-id="00e67-210">?</span><span class="sxs-lookup"><span data-stu-id="00e67-210">?</span></span>                         |



 

<span data-ttu-id="00e67-211">Le paramètre *charsetID* spécifie l’un des identificateurs de jeu de caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="00e67-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="00e67-212">Identificateur</span><span class="sxs-lookup"><span data-stu-id="00e67-212">Identifier</span></span> | <span data-ttu-id="00e67-213">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="00e67-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="00e67-214">0</span><span class="sxs-lookup"><span data-stu-id="00e67-214">0</span></span>          | <span data-ttu-id="00e67-215">ASCII 7 bits</span><span class="sxs-lookup"><span data-stu-id="00e67-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="00e67-216">932</span><span class="sxs-lookup"><span data-stu-id="00e67-216">932</span></span>        | <span data-ttu-id="00e67-217">Japon (Shift-JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="00e67-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="00e67-218">949</span><span class="sxs-lookup"><span data-stu-id="00e67-218">949</span></span>        | <span data-ttu-id="00e67-219">Corée (Shift-KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="00e67-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="00e67-220">950</span><span class="sxs-lookup"><span data-stu-id="00e67-220">950</span></span>        | <span data-ttu-id="00e67-221">Taïwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="00e67-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="00e67-222">1200</span><span class="sxs-lookup"><span data-stu-id="00e67-222">1200</span></span>       | <span data-ttu-id="00e67-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="00e67-223">Unicode</span></span>                    |
| <span data-ttu-id="00e67-224">1250</span><span class="sxs-lookup"><span data-stu-id="00e67-224">1250</span></span>       | <span data-ttu-id="00e67-225">Latin-2 (Europe de l’est)</span><span class="sxs-lookup"><span data-stu-id="00e67-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="00e67-226">1251</span><span class="sxs-lookup"><span data-stu-id="00e67-226">1251</span></span>       | <span data-ttu-id="00e67-227">Cyrillique</span><span class="sxs-lookup"><span data-stu-id="00e67-227">Cyrillic</span></span>                   |
| <span data-ttu-id="00e67-228">1252</span><span class="sxs-lookup"><span data-stu-id="00e67-228">1252</span></span>       | <span data-ttu-id="00e67-229">Multilingue</span><span class="sxs-lookup"><span data-stu-id="00e67-229">Multilingual</span></span>               |
| <span data-ttu-id="00e67-230">1253</span><span class="sxs-lookup"><span data-stu-id="00e67-230">1253</span></span>       | <span data-ttu-id="00e67-231">Grec</span><span class="sxs-lookup"><span data-stu-id="00e67-231">Greek</span></span>                      |
| <span data-ttu-id="00e67-232">1254</span><span class="sxs-lookup"><span data-stu-id="00e67-232">1254</span></span>       | <span data-ttu-id="00e67-233">Turc</span><span class="sxs-lookup"><span data-stu-id="00e67-233">Turkish</span></span>                    |
| <span data-ttu-id="00e67-234">1 255</span><span class="sxs-lookup"><span data-stu-id="00e67-234">1255</span></span>       | <span data-ttu-id="00e67-235">Hébreu</span><span class="sxs-lookup"><span data-stu-id="00e67-235">Hebrew</span></span>                     |
| <span data-ttu-id="00e67-236">1256</span><span class="sxs-lookup"><span data-stu-id="00e67-236">1256</span></span>       | <span data-ttu-id="00e67-237">Arabe</span><span class="sxs-lookup"><span data-stu-id="00e67-237">Arabic</span></span>                     |



 

 

 




