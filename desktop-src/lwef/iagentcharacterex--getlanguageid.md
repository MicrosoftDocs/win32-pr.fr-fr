---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120645"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="055d5-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="055d5-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="055d5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="055d5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="055d5-105">Récupère l’ID de langue défini pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="055d5-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="055d5-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="055d5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="055d5-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="055d5-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="055d5-108">Adresse d’une variable qui reçoit le paramètre ID de langue pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="055d5-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="055d5-109">Entier long spécifiant l’ID de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="055d5-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="055d5-110">L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="055d5-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="055d5-111">Les exemples suivants sont des valeurs pour certains langages.</span><span class="sxs-lookup"><span data-stu-id="055d5-111">The following examples are values for some languages.</span></span> <span data-ttu-id="055d5-112">Pour déterminer les valeurs d’autres langages, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="055d5-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="055d5-113">Langage</span><span class="sxs-lookup"><span data-stu-id="055d5-113">Language</span></span>              | <span data-ttu-id="055d5-114">id</span><span class="sxs-lookup"><span data-stu-id="055d5-114">ID</span></span>     | <span data-ttu-id="055d5-115">Langage</span><span class="sxs-lookup"><span data-stu-id="055d5-115">Language</span></span>              | <span data-ttu-id="055d5-116">id</span><span class="sxs-lookup"><span data-stu-id="055d5-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="055d5-117">Arabe (Arabie)</span><span class="sxs-lookup"><span data-stu-id="055d5-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="055d5-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="055d5-118">0x0401</span></span> | <span data-ttu-id="055d5-119">Italien</span><span class="sxs-lookup"><span data-stu-id="055d5-119">Italian</span></span>               | <span data-ttu-id="055d5-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="055d5-120">0x0410</span></span> |
| <span data-ttu-id="055d5-121">Basque</span><span class="sxs-lookup"><span data-stu-id="055d5-121">Basque</span></span>                | <span data-ttu-id="055d5-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="055d5-122">0x042d</span></span> | <span data-ttu-id="055d5-123">Japonais</span><span class="sxs-lookup"><span data-stu-id="055d5-123">Japanese</span></span>              | <span data-ttu-id="055d5-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="055d5-124">0x0411</span></span> |
| <span data-ttu-id="055d5-125">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="055d5-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="055d5-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="055d5-126">0x0804</span></span> | <span data-ttu-id="055d5-127">Coréen</span><span class="sxs-lookup"><span data-stu-id="055d5-127">Korean</span></span>                | <span data-ttu-id="055d5-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="055d5-128">0x0412</span></span> |
| <span data-ttu-id="055d5-129">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="055d5-129">Chinese (Traditional)</span></span> | <span data-ttu-id="055d5-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="055d5-130">0x0404</span></span> | <span data-ttu-id="055d5-131">Norvégien</span><span class="sxs-lookup"><span data-stu-id="055d5-131">Norwegian</span></span>             | <span data-ttu-id="055d5-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="055d5-132">0x0414</span></span> |
| <span data-ttu-id="055d5-133">Croate</span><span class="sxs-lookup"><span data-stu-id="055d5-133">Croatian</span></span>              | <span data-ttu-id="055d5-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="055d5-134">0x041A</span></span> | <span data-ttu-id="055d5-135">Polonais</span><span class="sxs-lookup"><span data-stu-id="055d5-135">Polish</span></span>                | <span data-ttu-id="055d5-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="055d5-136">0x0415</span></span> |
| <span data-ttu-id="055d5-137">Tchèque</span><span class="sxs-lookup"><span data-stu-id="055d5-137">Czech</span></span>                 | <span data-ttu-id="055d5-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="055d5-138">0x0405</span></span> | <span data-ttu-id="055d5-139">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="055d5-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="055d5-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="055d5-140">0x0816</span></span> |
| <span data-ttu-id="055d5-141">Danois</span><span class="sxs-lookup"><span data-stu-id="055d5-141">Danish</span></span>                | <span data-ttu-id="055d5-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="055d5-142">0x0406</span></span> | <span data-ttu-id="055d5-143">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="055d5-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="055d5-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="055d5-144">0x0416</span></span> |
| <span data-ttu-id="055d5-145">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="055d5-145">Dutch</span></span>                 | <span data-ttu-id="055d5-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="055d5-146">0x0413</span></span> | <span data-ttu-id="055d5-147">Roumain</span><span class="sxs-lookup"><span data-stu-id="055d5-147">Romanian</span></span>              | <span data-ttu-id="055d5-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="055d5-148">0x0418</span></span> |
| <span data-ttu-id="055d5-149">Anglais (Royaume-Uni)</span><span class="sxs-lookup"><span data-stu-id="055d5-149">English (British)</span></span>     | <span data-ttu-id="055d5-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="055d5-150">0x0809</span></span> | <span data-ttu-id="055d5-151">Russe</span><span class="sxs-lookup"><span data-stu-id="055d5-151">Russian</span></span>               | <span data-ttu-id="055d5-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="055d5-152">0x0419</span></span> |
| <span data-ttu-id="055d5-153">Anglais (US)</span><span class="sxs-lookup"><span data-stu-id="055d5-153">English (US)</span></span>          | <span data-ttu-id="055d5-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="055d5-154">0x0409</span></span> | <span data-ttu-id="055d5-155">Slovaque</span><span class="sxs-lookup"><span data-stu-id="055d5-155">Slovakian</span></span>             | <span data-ttu-id="055d5-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="055d5-156">0x041B</span></span> |
| <span data-ttu-id="055d5-157">Finnois</span><span class="sxs-lookup"><span data-stu-id="055d5-157">Finnish</span></span>               | <span data-ttu-id="055d5-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="055d5-158">0x040B</span></span> | <span data-ttu-id="055d5-159">Slovène</span><span class="sxs-lookup"><span data-stu-id="055d5-159">Slovenian</span></span>             | <span data-ttu-id="055d5-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="055d5-160">0x0424</span></span> |
| <span data-ttu-id="055d5-161">Français</span><span class="sxs-lookup"><span data-stu-id="055d5-161">French</span></span>                | <span data-ttu-id="055d5-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="055d5-162">0x040C</span></span> | <span data-ttu-id="055d5-163">Espagnol</span><span class="sxs-lookup"><span data-stu-id="055d5-163">Spanish</span></span>               | <span data-ttu-id="055d5-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="055d5-164">0x0C0A</span></span> |
| <span data-ttu-id="055d5-165">Allemand</span><span class="sxs-lookup"><span data-stu-id="055d5-165">German</span></span>                | <span data-ttu-id="055d5-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="055d5-166">0x0407</span></span> | <span data-ttu-id="055d5-167">Suédois</span><span class="sxs-lookup"><span data-stu-id="055d5-167">Swedish</span></span>               | <span data-ttu-id="055d5-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="055d5-168">0x041D</span></span> |
| <span data-ttu-id="055d5-169">Grec</span><span class="sxs-lookup"><span data-stu-id="055d5-169">Greek</span></span>                 | <span data-ttu-id="055d5-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="055d5-170">0x0408</span></span> | <span data-ttu-id="055d5-171">Thaï</span><span class="sxs-lookup"><span data-stu-id="055d5-171">Thai</span></span>                  | <span data-ttu-id="055d5-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="055d5-172">0x041E</span></span> |
| <span data-ttu-id="055d5-173">Hébreu</span><span class="sxs-lookup"><span data-stu-id="055d5-173">Hebrew</span></span>                | <span data-ttu-id="055d5-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="055d5-174">0x040D</span></span> | <span data-ttu-id="055d5-175">Turc</span><span class="sxs-lookup"><span data-stu-id="055d5-175">Turkish</span></span>               | <span data-ttu-id="055d5-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="055d5-176">0x041F</span></span> |
| <span data-ttu-id="055d5-177">Hongrois</span><span class="sxs-lookup"><span data-stu-id="055d5-177">Hungarian</span></span>             | <span data-ttu-id="055d5-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="055d5-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="055d5-179">Si vous ne définissez pas cet ID de langue pour le caractère, l’ID de langue du caractère sera l’ID de langue du système actuel.</span><span class="sxs-lookup"><span data-stu-id="055d5-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="055d5-180">Ce paramètre détermine également la langue pour la sortie TTS, le texte de la bulle, les commandes dans le menu contextuel du caractère et le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="055d5-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="055d5-181">Pour déterminer si un moteur de reconnaissance vocale compatible est disponible pour la langue du caractère, utilisez [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="055d5-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="055d5-182">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="055d5-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="055d5-183">Si l’ID de langue est défini sur une langue qui prend en charge le texte bidirectionnel (comme l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle installée, le texte apparaît dans le mot-bulle dans l’ordre logique plutôt que dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="055d5-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="055d5-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="055d5-184">See Also</span></span>

<span data-ttu-id="055d5-185">[**IAgentCharacterEx : SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="055d5-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




