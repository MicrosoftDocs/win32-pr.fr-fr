---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029567"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="68731-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="68731-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="68731-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68731-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="68731-105">Récupère l’ID de langue défini pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="68731-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="68731-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="68731-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="68731-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="68731-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="68731-108">Adresse d’une variable qui reçoit le paramètre ID de langue pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="68731-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="68731-109">Entier long spécifiant l’ID de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="68731-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="68731-110">L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="68731-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="68731-111">Les exemples suivants sont des valeurs pour certains langages.</span><span class="sxs-lookup"><span data-stu-id="68731-111">The following examples are values for some languages.</span></span> <span data-ttu-id="68731-112">Pour déterminer les valeurs d’autres langages, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="68731-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="68731-113">Arabe (Arabie)</span><span class="sxs-lookup"><span data-stu-id="68731-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="68731-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="68731-114">0x0401</span></span> | <span data-ttu-id="68731-115">Italien</span><span class="sxs-lookup"><span data-stu-id="68731-115">Italian</span></span>               | <span data-ttu-id="68731-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="68731-116">0x0410</span></span> |
| <span data-ttu-id="68731-117">Basque</span><span class="sxs-lookup"><span data-stu-id="68731-117">Basque</span></span>                | <span data-ttu-id="68731-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="68731-118">0x042d</span></span> | <span data-ttu-id="68731-119">Japonais</span><span class="sxs-lookup"><span data-stu-id="68731-119">Japanese</span></span>              | <span data-ttu-id="68731-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="68731-120">0x0411</span></span> |
| <span data-ttu-id="68731-121">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="68731-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="68731-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="68731-122">0x0804</span></span> | <span data-ttu-id="68731-123">Coréen</span><span class="sxs-lookup"><span data-stu-id="68731-123">Korean</span></span>                | <span data-ttu-id="68731-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="68731-124">0x0412</span></span> |
| <span data-ttu-id="68731-125">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="68731-125">Chinese (Traditional)</span></span> | <span data-ttu-id="68731-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="68731-126">0x0404</span></span> | <span data-ttu-id="68731-127">Norvégien</span><span class="sxs-lookup"><span data-stu-id="68731-127">Norwegian</span></span>             | <span data-ttu-id="68731-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="68731-128">0x0414</span></span> |
| <span data-ttu-id="68731-129">Croate</span><span class="sxs-lookup"><span data-stu-id="68731-129">Croatian</span></span>              | <span data-ttu-id="68731-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="68731-130">0x041A</span></span> | <span data-ttu-id="68731-131">Polonais</span><span class="sxs-lookup"><span data-stu-id="68731-131">Polish</span></span>                | <span data-ttu-id="68731-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="68731-132">0x0415</span></span> |
| <span data-ttu-id="68731-133">Tchèque</span><span class="sxs-lookup"><span data-stu-id="68731-133">Czech</span></span>                 | <span data-ttu-id="68731-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="68731-134">0x0405</span></span> | <span data-ttu-id="68731-135">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="68731-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="68731-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="68731-136">0x0816</span></span> |
| <span data-ttu-id="68731-137">Danois</span><span class="sxs-lookup"><span data-stu-id="68731-137">Danish</span></span>                | <span data-ttu-id="68731-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="68731-138">0x0406</span></span> | <span data-ttu-id="68731-139">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="68731-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="68731-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="68731-140">0x0416</span></span> |
| <span data-ttu-id="68731-141">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="68731-141">Dutch</span></span>                 | <span data-ttu-id="68731-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="68731-142">0x0413</span></span> | <span data-ttu-id="68731-143">Roumain</span><span class="sxs-lookup"><span data-stu-id="68731-143">Romanian</span></span>              | <span data-ttu-id="68731-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="68731-144">0x0418</span></span> |
| <span data-ttu-id="68731-145">Anglais (Royaume-Uni)</span><span class="sxs-lookup"><span data-stu-id="68731-145">English (British)</span></span>     | <span data-ttu-id="68731-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="68731-146">0x0809</span></span> | <span data-ttu-id="68731-147">Russe</span><span class="sxs-lookup"><span data-stu-id="68731-147">Russian</span></span>               | <span data-ttu-id="68731-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="68731-148">0x0419</span></span> |
| <span data-ttu-id="68731-149">Anglais (US)</span><span class="sxs-lookup"><span data-stu-id="68731-149">English (US)</span></span>          | <span data-ttu-id="68731-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="68731-150">0x0409</span></span> | <span data-ttu-id="68731-151">Slovaque</span><span class="sxs-lookup"><span data-stu-id="68731-151">Slovakian</span></span>             | <span data-ttu-id="68731-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="68731-152">0x041B</span></span> |
| <span data-ttu-id="68731-153">Finnois</span><span class="sxs-lookup"><span data-stu-id="68731-153">Finnish</span></span>               | <span data-ttu-id="68731-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="68731-154">0x040B</span></span> | <span data-ttu-id="68731-155">Slovène</span><span class="sxs-lookup"><span data-stu-id="68731-155">Slovenian</span></span>             | <span data-ttu-id="68731-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="68731-156">0x0424</span></span> |
| <span data-ttu-id="68731-157">Français</span><span class="sxs-lookup"><span data-stu-id="68731-157">French</span></span>                | <span data-ttu-id="68731-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="68731-158">0x040C</span></span> | <span data-ttu-id="68731-159">Espagnol</span><span class="sxs-lookup"><span data-stu-id="68731-159">Spanish</span></span>               | <span data-ttu-id="68731-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="68731-160">0x0C0A</span></span> |
| <span data-ttu-id="68731-161">Allemand</span><span class="sxs-lookup"><span data-stu-id="68731-161">German</span></span>                | <span data-ttu-id="68731-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="68731-162">0x0407</span></span> | <span data-ttu-id="68731-163">Suédois</span><span class="sxs-lookup"><span data-stu-id="68731-163">Swedish</span></span>               | <span data-ttu-id="68731-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="68731-164">0x041D</span></span> |
| <span data-ttu-id="68731-165">Grec</span><span class="sxs-lookup"><span data-stu-id="68731-165">Greek</span></span>                 | <span data-ttu-id="68731-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="68731-166">0x0408</span></span> | <span data-ttu-id="68731-167">Thaï</span><span class="sxs-lookup"><span data-stu-id="68731-167">Thai</span></span>                  | <span data-ttu-id="68731-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="68731-168">0x041E</span></span> |
| <span data-ttu-id="68731-169">Hébreu</span><span class="sxs-lookup"><span data-stu-id="68731-169">Hebrew</span></span>                | <span data-ttu-id="68731-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="68731-170">0x040D</span></span> | <span data-ttu-id="68731-171">Turc</span><span class="sxs-lookup"><span data-stu-id="68731-171">Turkish</span></span>               | <span data-ttu-id="68731-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="68731-172">0x041F</span></span> |
| <span data-ttu-id="68731-173">Hongrois</span><span class="sxs-lookup"><span data-stu-id="68731-173">Hungarian</span></span>             | <span data-ttu-id="68731-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="68731-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="68731-175">Si vous ne définissez pas cet ID de langue pour le caractère, l’ID de langue du caractère sera l’ID de langue du système actuel.</span><span class="sxs-lookup"><span data-stu-id="68731-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="68731-176">Ce paramètre détermine également la langue pour la sortie TTS, le texte de la bulle, les commandes dans le menu contextuel du caractère et le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="68731-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="68731-177">Pour déterminer si un moteur de reconnaissance vocale compatible est disponible pour la langue du caractère, utilisez [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="68731-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="68731-178">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="68731-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="68731-179">Si l’ID de langue est défini sur une langue qui prend en charge le texte bidirectionnel (comme l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle installée, le texte apparaît dans le mot-bulle dans l’ordre logique plutôt que dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="68731-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="68731-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68731-180">See Also</span></span>

<span data-ttu-id="68731-181">[**IAgentCharacterEx : SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="68731-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




