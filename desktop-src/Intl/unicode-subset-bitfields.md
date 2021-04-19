---
description: Les USBss de sous-ensemble Unicode sont utilisés dans les structures FONTSIGNATURE et LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Champs de décodage Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529308"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="31eb9-103">Champs de décodage Unicode</span><span class="sxs-lookup"><span data-stu-id="31eb9-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="31eb9-104">Les USBss de sous-ensemble Unicode sont utilisés dans les structures [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) et [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .</span><span class="sxs-lookup"><span data-stu-id="31eb9-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="31eb9-105">bit</span><span class="sxs-lookup"><span data-stu-id="31eb9-105">Bit</span></span></th>
<th><span data-ttu-id="31eb9-106">Sous-plage Unicode</span><span class="sxs-lookup"><span data-stu-id="31eb9-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="31eb9-107">Description</span><span class="sxs-lookup"><span data-stu-id="31eb9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31eb9-108">0</span><span class="sxs-lookup"><span data-stu-id="31eb9-108">0</span></span></td>
<td><span data-ttu-id="31eb9-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="31eb9-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="31eb9-110">Latin de base</span><span class="sxs-lookup"><span data-stu-id="31eb9-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-111">1</span><span class="sxs-lookup"><span data-stu-id="31eb9-111">1</span></span></td>
<td><span data-ttu-id="31eb9-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="31eb9-113">Supplément latin-1</span><span class="sxs-lookup"><span data-stu-id="31eb9-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-114">2</span><span class="sxs-lookup"><span data-stu-id="31eb9-114">2</span></span></td>
<td><span data-ttu-id="31eb9-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="31eb9-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="31eb9-116">Latin étendu-A</span><span class="sxs-lookup"><span data-stu-id="31eb9-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-117">3</span><span class="sxs-lookup"><span data-stu-id="31eb9-117">3</span></span></td>
<td><span data-ttu-id="31eb9-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="31eb9-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="31eb9-119">Latin étendu-B</span><span class="sxs-lookup"><span data-stu-id="31eb9-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="31eb9-120">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="31eb9-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="31eb9-122">Extensions de la Loi</span><span class="sxs-lookup"><span data-stu-id="31eb9-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="31eb9-124">Extensions phonétiques</span><span class="sxs-lookup"><span data-stu-id="31eb9-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="31eb9-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="31eb9-126">Supplément phonétique des extensions</span><span class="sxs-lookup"><span data-stu-id="31eb9-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-127">5 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="31eb9-129">Lettres du modificateur d’espacement</span><span class="sxs-lookup"><span data-stu-id="31eb9-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-130">A700 - A71F</span><span class="sxs-lookup"><span data-stu-id="31eb9-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="31eb9-131">Lettres de ton modificateur</span><span class="sxs-lookup"><span data-stu-id="31eb9-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-132">6 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="31eb9-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="31eb9-134">Combinaison de marques diacritiques</span><span class="sxs-lookup"><span data-stu-id="31eb9-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="31eb9-136">Supplément de marques diacritiques de combinaison</span><span class="sxs-lookup"><span data-stu-id="31eb9-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-137">7</span><span class="sxs-lookup"><span data-stu-id="31eb9-137">7</span></span></td>
<td><span data-ttu-id="31eb9-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="31eb9-139">Grec et copte</span><span class="sxs-lookup"><span data-stu-id="31eb9-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-140">8</span><span class="sxs-lookup"><span data-stu-id="31eb9-140">8</span></span></td>
<td><span data-ttu-id="31eb9-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="31eb9-142">Copte</span><span class="sxs-lookup"><span data-stu-id="31eb9-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="31eb9-143">9 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="31eb9-145">Cyrillique</span><span class="sxs-lookup"><span data-stu-id="31eb9-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="31eb9-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="31eb9-147">Supplément cyrillique</span><span class="sxs-lookup"><span data-stu-id="31eb9-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="31eb9-149">Cyrillique étendu-A</span><span class="sxs-lookup"><span data-stu-id="31eb9-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="31eb9-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="31eb9-151">Cyrillique étendu-B</span><span class="sxs-lookup"><span data-stu-id="31eb9-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-152">10</span><span class="sxs-lookup"><span data-stu-id="31eb9-152">10</span></span></td>
<td><span data-ttu-id="31eb9-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="31eb9-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="31eb9-154">Arménien</span><span class="sxs-lookup"><span data-stu-id="31eb9-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-155">11</span><span class="sxs-lookup"><span data-stu-id="31eb9-155">11</span></span></td>
<td><span data-ttu-id="31eb9-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="31eb9-157">Hébreu</span><span class="sxs-lookup"><span data-stu-id="31eb9-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-158">12</span><span class="sxs-lookup"><span data-stu-id="31eb9-158">12</span></span></td>
<td><span data-ttu-id="31eb9-159">A500 - A63F</span><span class="sxs-lookup"><span data-stu-id="31eb9-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="31eb9-160">Vaï</span><span class="sxs-lookup"><span data-stu-id="31eb9-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-161">13 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="31eb9-163">Arabe</span><span class="sxs-lookup"><span data-stu-id="31eb9-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="31eb9-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="31eb9-165">Supplément arabe</span><span class="sxs-lookup"><span data-stu-id="31eb9-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-166">14</span><span class="sxs-lookup"><span data-stu-id="31eb9-166">14</span></span></td>
<td><span data-ttu-id="31eb9-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="31eb9-168">GBA</span><span class="sxs-lookup"><span data-stu-id="31eb9-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-169">15</span><span class="sxs-lookup"><span data-stu-id="31eb9-169">15</span></span></td>
<td><span data-ttu-id="31eb9-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="31eb9-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="31eb9-171">Dévanâgarî</span><span class="sxs-lookup"><span data-stu-id="31eb9-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-172">16</span><span class="sxs-lookup"><span data-stu-id="31eb9-172">16</span></span></td>
<td><span data-ttu-id="31eb9-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="31eb9-174">Bangla</span><span class="sxs-lookup"><span data-stu-id="31eb9-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-175">17</span><span class="sxs-lookup"><span data-stu-id="31eb9-175">17</span></span></td>
<td><span data-ttu-id="31eb9-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="31eb9-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="31eb9-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-178">18</span><span class="sxs-lookup"><span data-stu-id="31eb9-178">18</span></span></td>
<td><span data-ttu-id="31eb9-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="31eb9-180">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="31eb9-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-181">19</span><span class="sxs-lookup"><span data-stu-id="31eb9-181">19</span></span></td>
<td><span data-ttu-id="31eb9-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="31eb9-183">Odia</span><span class="sxs-lookup"><span data-stu-id="31eb9-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-184">20</span><span class="sxs-lookup"><span data-stu-id="31eb9-184">20</span></span></td>
<td><span data-ttu-id="31eb9-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="31eb9-186">Tamoul</span><span class="sxs-lookup"><span data-stu-id="31eb9-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-187">21</span><span class="sxs-lookup"><span data-stu-id="31eb9-187">21</span></span></td>
<td><span data-ttu-id="31eb9-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="31eb9-189">Télougou</span><span class="sxs-lookup"><span data-stu-id="31eb9-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-190">22</span><span class="sxs-lookup"><span data-stu-id="31eb9-190">22</span></span></td>
<td><span data-ttu-id="31eb9-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="31eb9-192">Kannada</span><span class="sxs-lookup"><span data-stu-id="31eb9-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-193">23</span><span class="sxs-lookup"><span data-stu-id="31eb9-193">23</span></span></td>
<td><span data-ttu-id="31eb9-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="31eb9-195">Malayalam</span><span class="sxs-lookup"><span data-stu-id="31eb9-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-196">24</span><span class="sxs-lookup"><span data-stu-id="31eb9-196">24</span></span></td>
<td><span data-ttu-id="31eb9-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="31eb9-198">Thaï</span><span class="sxs-lookup"><span data-stu-id="31eb9-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-199">25</span><span class="sxs-lookup"><span data-stu-id="31eb9-199">25</span></span></td>
<td><span data-ttu-id="31eb9-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="31eb9-201">Lao</span><span class="sxs-lookup"><span data-stu-id="31eb9-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-202">26 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="31eb9-204">Géorgien</span><span class="sxs-lookup"><span data-stu-id="31eb9-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="31eb9-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="31eb9-206">Supplément géorgien</span><span class="sxs-lookup"><span data-stu-id="31eb9-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-207">27</span><span class="sxs-lookup"><span data-stu-id="31eb9-207">27</span></span></td>
<td><span data-ttu-id="31eb9-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="31eb9-209">Balinais</span><span class="sxs-lookup"><span data-stu-id="31eb9-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-210">28</span><span class="sxs-lookup"><span data-stu-id="31eb9-210">28</span></span></td>
<td><span data-ttu-id="31eb9-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="31eb9-212">Hangul Jamos</span><span class="sxs-lookup"><span data-stu-id="31eb9-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="31eb9-213">29 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="31eb9-215">Latin étendu additionnel</span><span class="sxs-lookup"><span data-stu-id="31eb9-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="31eb9-217">Latin étendu-C</span><span class="sxs-lookup"><span data-stu-id="31eb9-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="31eb9-219">Latin étendu-D</span><span class="sxs-lookup"><span data-stu-id="31eb9-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-220">30</span><span class="sxs-lookup"><span data-stu-id="31eb9-220">30</span></span></td>
<td><span data-ttu-id="31eb9-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="31eb9-222">Grec étendu</span><span class="sxs-lookup"><span data-stu-id="31eb9-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-223">31 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="31eb9-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="31eb9-225">Ponctuation générale</span><span class="sxs-lookup"><span data-stu-id="31eb9-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="31eb9-227">Ponctuation supplémentaire</span><span class="sxs-lookup"><span data-stu-id="31eb9-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-228">32</span><span class="sxs-lookup"><span data-stu-id="31eb9-228">32</span></span></td>
<td><span data-ttu-id="31eb9-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="31eb9-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="31eb9-230">Exposants et indices</span><span class="sxs-lookup"><span data-stu-id="31eb9-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-231">33</span><span class="sxs-lookup"><span data-stu-id="31eb9-231">33</span></span></td>
<td><span data-ttu-id="31eb9-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="31eb9-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="31eb9-233">Symboles monétaires</span><span class="sxs-lookup"><span data-stu-id="31eb9-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-234">34</span><span class="sxs-lookup"><span data-stu-id="31eb9-234">34</span></span></td>
<td><span data-ttu-id="31eb9-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="31eb9-236">Combinaison de signes diacritiques pour les symboles</span><span class="sxs-lookup"><span data-stu-id="31eb9-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-237">35</span><span class="sxs-lookup"><span data-stu-id="31eb9-237">35</span></span></td>
<td><span data-ttu-id="31eb9-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="31eb9-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="31eb9-239">Symboles type lettre</span><span class="sxs-lookup"><span data-stu-id="31eb9-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-240">36</span><span class="sxs-lookup"><span data-stu-id="31eb9-240">36</span></span></td>
<td><span data-ttu-id="31eb9-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="31eb9-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="31eb9-242">Formats de nombres</span><span class="sxs-lookup"><span data-stu-id="31eb9-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="31eb9-243">37 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="31eb9-245">Flèches</span><span class="sxs-lookup"><span data-stu-id="31eb9-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="31eb9-247">Flèches supplémentaires-A</span><span class="sxs-lookup"><span data-stu-id="31eb9-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="31eb9-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="31eb9-249">Flèches supplémentaires-B</span><span class="sxs-lookup"><span data-stu-id="31eb9-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="31eb9-251">Symboles et flèches divers</span><span class="sxs-lookup"><span data-stu-id="31eb9-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="31eb9-252">38 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="31eb9-254">Opérateurs mathématiques</span><span class="sxs-lookup"><span data-stu-id="31eb9-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="31eb9-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="31eb9-256">Symboles mathématiques divers-A</span><span class="sxs-lookup"><span data-stu-id="31eb9-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="31eb9-258">Divers symboles mathématiques-B</span><span class="sxs-lookup"><span data-stu-id="31eb9-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="31eb9-260">Opérateurs mathématiques supplémentaires</span><span class="sxs-lookup"><span data-stu-id="31eb9-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-261">39</span><span class="sxs-lookup"><span data-stu-id="31eb9-261">39</span></span></td>
<td><span data-ttu-id="31eb9-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="31eb9-263">Autres techniques</span><span class="sxs-lookup"><span data-stu-id="31eb9-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-264">40</span><span class="sxs-lookup"><span data-stu-id="31eb9-264">40</span></span></td>
<td><span data-ttu-id="31eb9-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="31eb9-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="31eb9-266">Images de contrôle</span><span class="sxs-lookup"><span data-stu-id="31eb9-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-267">41</span><span class="sxs-lookup"><span data-stu-id="31eb9-267">41</span></span></td>
<td><span data-ttu-id="31eb9-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="31eb9-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="31eb9-269">Reconnaissance optique de caractères</span><span class="sxs-lookup"><span data-stu-id="31eb9-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-270">42</span><span class="sxs-lookup"><span data-stu-id="31eb9-270">42</span></span></td>
<td><span data-ttu-id="31eb9-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="31eb9-272">Alphanumériques encadrés</span><span class="sxs-lookup"><span data-stu-id="31eb9-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-273">43</span><span class="sxs-lookup"><span data-stu-id="31eb9-273">43</span></span></td>
<td><span data-ttu-id="31eb9-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="31eb9-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="31eb9-275">Dessin Box</span><span class="sxs-lookup"><span data-stu-id="31eb9-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-276">44</span><span class="sxs-lookup"><span data-stu-id="31eb9-276">44</span></span></td>
<td><span data-ttu-id="31eb9-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="31eb9-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="31eb9-278">Éléments de bloc</span><span class="sxs-lookup"><span data-stu-id="31eb9-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-279">45</span><span class="sxs-lookup"><span data-stu-id="31eb9-279">45</span></span></td>
<td><span data-ttu-id="31eb9-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="31eb9-281">Formes géométriques</span><span class="sxs-lookup"><span data-stu-id="31eb9-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-282">46</span><span class="sxs-lookup"><span data-stu-id="31eb9-282">46</span></span></td>
<td><span data-ttu-id="31eb9-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="31eb9-284">Symboles divers</span><span class="sxs-lookup"><span data-stu-id="31eb9-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-285">47</span><span class="sxs-lookup"><span data-stu-id="31eb9-285">47</span></span></td>
<td><span data-ttu-id="31eb9-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="31eb9-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="31eb9-287">Casseau</span><span class="sxs-lookup"><span data-stu-id="31eb9-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-288">48</span><span class="sxs-lookup"><span data-stu-id="31eb9-288">48</span></span></td>
<td><span data-ttu-id="31eb9-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="31eb9-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="31eb9-290">Symboles et ponctuation CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-291">49</span><span class="sxs-lookup"><span data-stu-id="31eb9-291">49</span></span></td>
<td><span data-ttu-id="31eb9-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="31eb9-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="31eb9-293">Hiragana</span><span class="sxs-lookup"><span data-stu-id="31eb9-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-294">50 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="31eb9-296">Katakana</span><span class="sxs-lookup"><span data-stu-id="31eb9-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="31eb9-298">Extensions phonétiques katakana</span><span class="sxs-lookup"><span data-stu-id="31eb9-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-299">51 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="31eb9-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="31eb9-301">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="31eb9-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="31eb9-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="31eb9-303">Bopomofo étendu</span><span class="sxs-lookup"><span data-stu-id="31eb9-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-304">52</span><span class="sxs-lookup"><span data-stu-id="31eb9-304">52</span></span></td>
<td><span data-ttu-id="31eb9-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="31eb9-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="31eb9-306">Jamos de compatibilité HANGÛL</span><span class="sxs-lookup"><span data-stu-id="31eb9-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-307">53</span><span class="sxs-lookup"><span data-stu-id="31eb9-307">53</span></span></td>
<td><span data-ttu-id="31eb9-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="31eb9-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="31eb9-309">PHAGS-PA</span><span class="sxs-lookup"><span data-stu-id="31eb9-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-310">54</span><span class="sxs-lookup"><span data-stu-id="31eb9-310">54</span></span></td>
<td><span data-ttu-id="31eb9-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="31eb9-312">Lettres et mois CJC entre parenthèses</span><span class="sxs-lookup"><span data-stu-id="31eb9-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-313">55</span><span class="sxs-lookup"><span data-stu-id="31eb9-313">55</span></span></td>
<td><span data-ttu-id="31eb9-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="31eb9-315">COMPATIBILITÉ CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-316">56</span><span class="sxs-lookup"><span data-stu-id="31eb9-316">56</span></span></td>
<td><span data-ttu-id="31eb9-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="31eb9-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="31eb9-318">Syllabes Hangul</span><span class="sxs-lookup"><span data-stu-id="31eb9-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-319">57</span><span class="sxs-lookup"><span data-stu-id="31eb9-319">57</span></span></td>
<td><span data-ttu-id="31eb9-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="31eb9-321">Non-plan 0.</span><span class="sxs-lookup"><span data-stu-id="31eb9-321">Non-Plane 0.</span></span> <span data-ttu-id="31eb9-322">Notez que la définition de ce bit implique qu’il existe au moins un point de code supplémentaire au-delà du plan multilingue de base (BMP) pris en charge par cette police.</span><span class="sxs-lookup"><span data-stu-id="31eb9-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="31eb9-323">Consultez <a href="surrogates-and-supplementary-characters.md">substituts et caractères supplémentaires</a>.</span><span class="sxs-lookup"><span data-stu-id="31eb9-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-324">58</span><span class="sxs-lookup"><span data-stu-id="31eb9-324">58</span></span></td>
<td><span data-ttu-id="31eb9-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="31eb9-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="31eb9-326">Phéniciennes</span><span class="sxs-lookup"><span data-stu-id="31eb9-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="31eb9-327">59 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="31eb9-329">Complément des radicaux CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="31eb9-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="31eb9-331">Clé chinoise</span><span class="sxs-lookup"><span data-stu-id="31eb9-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="31eb9-333">Caractères de description IDÉOGRAPHIQUE</span><span class="sxs-lookup"><span data-stu-id="31eb9-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="31eb9-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="31eb9-335">Kanbun</span><span class="sxs-lookup"><span data-stu-id="31eb9-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="31eb9-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="31eb9-337">Extension de idéogrammes unifiés CJC A</span><span class="sxs-lookup"><span data-stu-id="31eb9-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="31eb9-339">Idéogrammes unifiés CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="31eb9-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="31eb9-341">Extension B des idéogrammes unifiés CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-342">60</span><span class="sxs-lookup"><span data-stu-id="31eb9-342">60</span></span></td>
<td><span data-ttu-id="31eb9-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="31eb9-344">Zone d’utilisation privée</span><span class="sxs-lookup"><span data-stu-id="31eb9-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="31eb9-345">61 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="31eb9-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="31eb9-347">Traits CJK</span><span class="sxs-lookup"><span data-stu-id="31eb9-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="31eb9-349">Idéogrammes de compatibilité CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="31eb9-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="31eb9-351">Complément idéogrammes de compatibilité CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-352">62</span><span class="sxs-lookup"><span data-stu-id="31eb9-352">62</span></span></td>
<td><span data-ttu-id="31eb9-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="31eb9-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="31eb9-354">Formes de présentation alphabétique</span><span class="sxs-lookup"><span data-stu-id="31eb9-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-355">63</span><span class="sxs-lookup"><span data-stu-id="31eb9-355">63</span></span></td>
<td><span data-ttu-id="31eb9-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="31eb9-357">Formulaires de présentation en arabe-A</span><span class="sxs-lookup"><span data-stu-id="31eb9-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-358">64</span><span class="sxs-lookup"><span data-stu-id="31eb9-358">64</span></span></td>
<td><span data-ttu-id="31eb9-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="31eb9-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="31eb9-360">Combinaison de demi-marques</span><span class="sxs-lookup"><span data-stu-id="31eb9-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-361">65 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="31eb9-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="31eb9-363">Formes verticales</span><span class="sxs-lookup"><span data-stu-id="31eb9-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="31eb9-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="31eb9-365">Formulaires de compatibilité CJC</span><span class="sxs-lookup"><span data-stu-id="31eb9-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-366">66</span><span class="sxs-lookup"><span data-stu-id="31eb9-366">66</span></span></td>
<td><span data-ttu-id="31eb9-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="31eb9-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="31eb9-368">Petites variantes de forme</span><span class="sxs-lookup"><span data-stu-id="31eb9-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-369">67</span><span class="sxs-lookup"><span data-stu-id="31eb9-369">67</span></span></td>
<td><span data-ttu-id="31eb9-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="31eb9-371">Formulaires de présentation arabes-B</span><span class="sxs-lookup"><span data-stu-id="31eb9-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-372">68</span><span class="sxs-lookup"><span data-stu-id="31eb9-372">68</span></span></td>
<td><span data-ttu-id="31eb9-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="31eb9-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="31eb9-374">Formes demi-chasse et pleine chasse</span><span class="sxs-lookup"><span data-stu-id="31eb9-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-375">69</span><span class="sxs-lookup"><span data-stu-id="31eb9-375">69</span></span></td>
<td><span data-ttu-id="31eb9-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="31eb9-377">Offres spéciales</span><span class="sxs-lookup"><span data-stu-id="31eb9-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-378">70</span><span class="sxs-lookup"><span data-stu-id="31eb9-378">70</span></span></td>
<td><span data-ttu-id="31eb9-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="31eb9-380">Tibétain</span><span class="sxs-lookup"><span data-stu-id="31eb9-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-381">71</span><span class="sxs-lookup"><span data-stu-id="31eb9-381">71</span></span></td>
<td><span data-ttu-id="31eb9-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="31eb9-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="31eb9-383">Syriaque</span><span class="sxs-lookup"><span data-stu-id="31eb9-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-384">72</span><span class="sxs-lookup"><span data-stu-id="31eb9-384">72</span></span></td>
<td><span data-ttu-id="31eb9-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="31eb9-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="31eb9-386">Tana</span><span class="sxs-lookup"><span data-stu-id="31eb9-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-387">73</span><span class="sxs-lookup"><span data-stu-id="31eb9-387">73</span></span></td>
<td><span data-ttu-id="31eb9-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="31eb9-389">Cingalais</span><span class="sxs-lookup"><span data-stu-id="31eb9-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-390">74</span><span class="sxs-lookup"><span data-stu-id="31eb9-390">74</span></span></td>
<td><span data-ttu-id="31eb9-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="31eb9-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="31eb9-392">Myanmar</span><span class="sxs-lookup"><span data-stu-id="31eb9-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="31eb9-393">75 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="31eb9-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="31eb9-395">Éthiopien</span><span class="sxs-lookup"><span data-stu-id="31eb9-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="31eb9-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="31eb9-397">Supplément éthiopien</span><span class="sxs-lookup"><span data-stu-id="31eb9-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="31eb9-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="31eb9-399">Éthiopien étendu</span><span class="sxs-lookup"><span data-stu-id="31eb9-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-400">76</span><span class="sxs-lookup"><span data-stu-id="31eb9-400">76</span></span></td>
<td><span data-ttu-id="31eb9-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="31eb9-402">Cherokee</span><span class="sxs-lookup"><span data-stu-id="31eb9-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-403">77</span><span class="sxs-lookup"><span data-stu-id="31eb9-403">77</span></span></td>
<td><span data-ttu-id="31eb9-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="31eb9-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="31eb9-405">SYLLABE autochtones canadienne</span><span class="sxs-lookup"><span data-stu-id="31eb9-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-406">78</span><span class="sxs-lookup"><span data-stu-id="31eb9-406">78</span></span></td>
<td><span data-ttu-id="31eb9-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="31eb9-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="31eb9-408">OGAM</span><span class="sxs-lookup"><span data-stu-id="31eb9-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-409">79</span><span class="sxs-lookup"><span data-stu-id="31eb9-409">79</span></span></td>
<td><span data-ttu-id="31eb9-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="31eb9-411">Lettre</span><span class="sxs-lookup"><span data-stu-id="31eb9-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-412">80 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="31eb9-414">Khmer</span><span class="sxs-lookup"><span data-stu-id="31eb9-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="31eb9-416">Symboles khmer</span><span class="sxs-lookup"><span data-stu-id="31eb9-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-417">81</span><span class="sxs-lookup"><span data-stu-id="31eb9-417">81</span></span></td>
<td><span data-ttu-id="31eb9-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="31eb9-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="31eb9-419">Mongol</span><span class="sxs-lookup"><span data-stu-id="31eb9-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-420">82</span><span class="sxs-lookup"><span data-stu-id="31eb9-420">82</span></span></td>
<td><span data-ttu-id="31eb9-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="31eb9-422">Modèles braille</span><span class="sxs-lookup"><span data-stu-id="31eb9-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-423">83 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="31eb9-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="31eb9-425">Syllabes Yi</span><span class="sxs-lookup"><span data-stu-id="31eb9-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="31eb9-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="31eb9-427">Radicaux Yi</span><span class="sxs-lookup"><span data-stu-id="31eb9-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="31eb9-428">84 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="31eb9-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="31eb9-430">Tagalog</span><span class="sxs-lookup"><span data-stu-id="31eb9-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="31eb9-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="31eb9-432">HANOUNÓO</span><span class="sxs-lookup"><span data-stu-id="31eb9-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="31eb9-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="31eb9-434">Bouhid</span><span class="sxs-lookup"><span data-stu-id="31eb9-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="31eb9-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="31eb9-436">Tagbanwa</span><span class="sxs-lookup"><span data-stu-id="31eb9-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-437">85 %</span><span class="sxs-lookup"><span data-stu-id="31eb9-437">85</span></span></td>
<td><span data-ttu-id="31eb9-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="31eb9-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="31eb9-439">Ancien italique</span><span class="sxs-lookup"><span data-stu-id="31eb9-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-440">86</span><span class="sxs-lookup"><span data-stu-id="31eb9-440">86</span></span></td>
<td><span data-ttu-id="31eb9-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="31eb9-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="31eb9-442">La</span><span class="sxs-lookup"><span data-stu-id="31eb9-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-443">87</span><span class="sxs-lookup"><span data-stu-id="31eb9-443">87</span></span></td>
<td><span data-ttu-id="31eb9-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="31eb9-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="31eb9-445">Deseret</span><span class="sxs-lookup"><span data-stu-id="31eb9-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="31eb9-446">88 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="31eb9-448">Symboles musicaux byzantines</span><span class="sxs-lookup"><span data-stu-id="31eb9-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="31eb9-450">Symboles musicaux</span><span class="sxs-lookup"><span data-stu-id="31eb9-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="31eb9-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="31eb9-452">Vieilles notation musicale grecque</span><span class="sxs-lookup"><span data-stu-id="31eb9-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-453">89</span><span class="sxs-lookup"><span data-stu-id="31eb9-453">89</span></span></td>
<td><span data-ttu-id="31eb9-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="31eb9-455">Symboles alphanumériques mathématiques</span><span class="sxs-lookup"><span data-stu-id="31eb9-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-456">90 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-457">FF000 - FFFFD</span><span class="sxs-lookup"><span data-stu-id="31eb9-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="31eb9-458">Utilisation privée (plan 15)</span><span class="sxs-lookup"><span data-stu-id="31eb9-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="31eb9-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="31eb9-460">Utilisation privée (plan 16)</span><span class="sxs-lookup"><span data-stu-id="31eb9-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-461">91 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="31eb9-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="31eb9-463">Sélecteurs de variante</span><span class="sxs-lookup"><span data-stu-id="31eb9-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="31eb9-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="31eb9-465">Complément sélecteurs de variante</span><span class="sxs-lookup"><span data-stu-id="31eb9-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-466">92</span><span class="sxs-lookup"><span data-stu-id="31eb9-466">92</span></span></td>
<td><span data-ttu-id="31eb9-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="31eb9-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="31eb9-468">Balises</span><span class="sxs-lookup"><span data-stu-id="31eb9-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-469">93</span><span class="sxs-lookup"><span data-stu-id="31eb9-469">93</span></span></td>
<td><span data-ttu-id="31eb9-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="31eb9-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="31eb9-471">Limbu</span><span class="sxs-lookup"><span data-stu-id="31eb9-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-472">94</span><span class="sxs-lookup"><span data-stu-id="31eb9-472">94</span></span></td>
<td><span data-ttu-id="31eb9-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="31eb9-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="31eb9-474">LETTRE TAÏ le</span><span class="sxs-lookup"><span data-stu-id="31eb9-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-475">95</span><span class="sxs-lookup"><span data-stu-id="31eb9-475">95</span></span></td>
<td><span data-ttu-id="31eb9-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="31eb9-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="31eb9-477">Nouveau taï lü</span><span class="sxs-lookup"><span data-stu-id="31eb9-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-478">96</span><span class="sxs-lookup"><span data-stu-id="31eb9-478">96</span></span></td>
<td><span data-ttu-id="31eb9-479">1A00-1A1F</span><span class="sxs-lookup"><span data-stu-id="31eb9-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="31eb9-480">Bugi</span><span class="sxs-lookup"><span data-stu-id="31eb9-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-481">97</span><span class="sxs-lookup"><span data-stu-id="31eb9-481">97</span></span></td>
<td><span data-ttu-id="31eb9-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="31eb9-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="31eb9-483">Lettre</span><span class="sxs-lookup"><span data-stu-id="31eb9-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-484">98</span><span class="sxs-lookup"><span data-stu-id="31eb9-484">98</span></span></td>
<td><span data-ttu-id="31eb9-485">2D30 - 2D7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="31eb9-486">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="31eb9-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-487">99</span><span class="sxs-lookup"><span data-stu-id="31eb9-487">99</span></span></td>
<td><span data-ttu-id="31eb9-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="31eb9-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="31eb9-489">Symboles de hexagramme hexagrammes</span><span class="sxs-lookup"><span data-stu-id="31eb9-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-490">100</span><span class="sxs-lookup"><span data-stu-id="31eb9-490">100</span></span></td>
<td><span data-ttu-id="31eb9-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="31eb9-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="31eb9-492">SYLOTÎ NÂGRÎ</span><span class="sxs-lookup"><span data-stu-id="31eb9-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="31eb9-493">101 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="31eb9-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="31eb9-495">SYLLABE B linéaire B</span><span class="sxs-lookup"><span data-stu-id="31eb9-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="31eb9-497">Idéogrammes linéaire B</span><span class="sxs-lookup"><span data-stu-id="31eb9-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="31eb9-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="31eb9-499">Chiffres des mer</span><span class="sxs-lookup"><span data-stu-id="31eb9-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-500">102</span><span class="sxs-lookup"><span data-stu-id="31eb9-500">102</span></span></td>
<td><span data-ttu-id="31eb9-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="31eb9-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="31eb9-502">Anciens nombres grecs</span><span class="sxs-lookup"><span data-stu-id="31eb9-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-503">103</span><span class="sxs-lookup"><span data-stu-id="31eb9-503">103</span></span></td>
<td><span data-ttu-id="31eb9-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="31eb9-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="31eb9-505">Ougaritique</span><span class="sxs-lookup"><span data-stu-id="31eb9-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-506">104</span><span class="sxs-lookup"><span data-stu-id="31eb9-506">104</span></span></td>
<td><span data-ttu-id="31eb9-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="31eb9-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="31eb9-508">Ancien persan</span><span class="sxs-lookup"><span data-stu-id="31eb9-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-509">105</span><span class="sxs-lookup"><span data-stu-id="31eb9-509">105</span></span></td>
<td><span data-ttu-id="31eb9-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="31eb9-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="31eb9-511">Copeaux</span><span class="sxs-lookup"><span data-stu-id="31eb9-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-512">106</span><span class="sxs-lookup"><span data-stu-id="31eb9-512">106</span></span></td>
<td><span data-ttu-id="31eb9-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="31eb9-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="31eb9-514">Osmanya</span><span class="sxs-lookup"><span data-stu-id="31eb9-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-515">107</span><span class="sxs-lookup"><span data-stu-id="31eb9-515">107</span></span></td>
<td><span data-ttu-id="31eb9-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="31eb9-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="31eb9-517">SYLLABE Cypriot</span><span class="sxs-lookup"><span data-stu-id="31eb9-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-518">108</span><span class="sxs-lookup"><span data-stu-id="31eb9-518">108</span></span></td>
<td><span data-ttu-id="31eb9-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="31eb9-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="31eb9-520">Kharoshthi</span><span class="sxs-lookup"><span data-stu-id="31eb9-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-521">109</span><span class="sxs-lookup"><span data-stu-id="31eb9-521">109</span></span></td>
<td><span data-ttu-id="31eb9-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="31eb9-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="31eb9-523">Symboles Taï Xuan Jing</span><span class="sxs-lookup"><span data-stu-id="31eb9-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="31eb9-524">110 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="31eb9-526">Cuneiform</span><span class="sxs-lookup"><span data-stu-id="31eb9-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="31eb9-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="31eb9-528">Nombres Cuneiform et ponctuation</span><span class="sxs-lookup"><span data-stu-id="31eb9-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-529">111</span><span class="sxs-lookup"><span data-stu-id="31eb9-529">111</span></span></td>
<td><span data-ttu-id="31eb9-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="31eb9-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="31eb9-531">Comptage des chiffres de la baguette</span><span class="sxs-lookup"><span data-stu-id="31eb9-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-532">112</span><span class="sxs-lookup"><span data-stu-id="31eb9-532">112</span></span></td>
<td><span data-ttu-id="31eb9-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="31eb9-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="31eb9-534">Soundanais</span><span class="sxs-lookup"><span data-stu-id="31eb9-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-535">113</span><span class="sxs-lookup"><span data-stu-id="31eb9-535">113</span></span></td>
<td><span data-ttu-id="31eb9-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="31eb9-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="31eb9-537">Lepcha</span><span class="sxs-lookup"><span data-stu-id="31eb9-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-538">114</span><span class="sxs-lookup"><span data-stu-id="31eb9-538">114</span></span></td>
<td><span data-ttu-id="31eb9-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="31eb9-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="31eb9-540">Ol tchiki</span><span class="sxs-lookup"><span data-stu-id="31eb9-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-541">115</span><span class="sxs-lookup"><span data-stu-id="31eb9-541">115</span></span></td>
<td><span data-ttu-id="31eb9-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="31eb9-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="31eb9-543">Saurashtra</span><span class="sxs-lookup"><span data-stu-id="31eb9-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-544">116</span><span class="sxs-lookup"><span data-stu-id="31eb9-544">116</span></span></td>
<td><span data-ttu-id="31eb9-545">A900 - A92F</span><span class="sxs-lookup"><span data-stu-id="31eb9-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="31eb9-546">Kayah Li</span><span class="sxs-lookup"><span data-stu-id="31eb9-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-547">117</span><span class="sxs-lookup"><span data-stu-id="31eb9-547">117</span></span></td>
<td><span data-ttu-id="31eb9-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="31eb9-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="31eb9-549">Rejang</span><span class="sxs-lookup"><span data-stu-id="31eb9-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-550">118</span><span class="sxs-lookup"><span data-stu-id="31eb9-550">118</span></span></td>
<td><span data-ttu-id="31eb9-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="31eb9-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="31eb9-552">Cham</span><span class="sxs-lookup"><span data-stu-id="31eb9-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-553">119</span><span class="sxs-lookup"><span data-stu-id="31eb9-553">119</span></span></td>
<td><span data-ttu-id="31eb9-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="31eb9-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="31eb9-555">Anciens symboles</span><span class="sxs-lookup"><span data-stu-id="31eb9-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-556">120</span><span class="sxs-lookup"><span data-stu-id="31eb9-556">120</span></span></td>
<td><span data-ttu-id="31eb9-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="31eb9-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="31eb9-558">Disque Phaistos</span><span class="sxs-lookup"><span data-stu-id="31eb9-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="31eb9-559">121 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="31eb9-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="31eb9-561">Lycien</span><span class="sxs-lookup"><span data-stu-id="31eb9-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="31eb9-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="31eb9-563">Carien</span><span class="sxs-lookup"><span data-stu-id="31eb9-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="31eb9-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="31eb9-565">Lydien</span><span class="sxs-lookup"><span data-stu-id="31eb9-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="31eb9-566">122 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="31eb9-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="31eb9-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="31eb9-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="31eb9-568">Vignettes de Mahjong</span><span class="sxs-lookup"><span data-stu-id="31eb9-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="31eb9-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="31eb9-570">Vignettes Domino</span><span class="sxs-lookup"><span data-stu-id="31eb9-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-571">123</span><span class="sxs-lookup"><span data-stu-id="31eb9-571">123</span></span></td>

<td><span data-ttu-id="31eb9-572"><strong>Windows 2000 et versions ultérieures :</strong> Disposition en cours, horizontal de droite à gauche</span><span class="sxs-lookup"><span data-stu-id="31eb9-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-573">124</span><span class="sxs-lookup"><span data-stu-id="31eb9-573">124</span></span></td>

<td><span data-ttu-id="31eb9-574"><strong>Windows 2000 et versions ultérieures :</strong> Mise en page en cours, vertical avant horizontal</span><span class="sxs-lookup"><span data-stu-id="31eb9-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31eb9-575">125</span><span class="sxs-lookup"><span data-stu-id="31eb9-575">125</span></span></td>

<td><span data-ttu-id="31eb9-576"><strong>Windows 2000 et versions ultérieures :</strong> Progression de la mise en page, de bas en haut</span><span class="sxs-lookup"><span data-stu-id="31eb9-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31eb9-577">126-127</span><span class="sxs-lookup"><span data-stu-id="31eb9-577">126-127</span></span></td>

<td><span data-ttu-id="31eb9-578">Réservé pour le processus-utilisation interne</span><span class="sxs-lookup"><span data-stu-id="31eb9-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



