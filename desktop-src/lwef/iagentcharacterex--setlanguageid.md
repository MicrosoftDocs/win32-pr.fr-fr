---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672118"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="950c3-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="950c3-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="950c3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="950c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="950c3-105">Définit l’ID de langue défini pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="950c3-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="950c3-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="950c3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="950c3-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="950c3-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="950c3-108">Paramètre de l’ID de langue pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="950c3-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="950c3-109">Entier long spécifiant l’ID de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="950c3-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="950c3-110">L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="950c3-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="950c3-111">Vous pouvez utiliser les valeurs suivantes pour les langues spécifiées.</span><span class="sxs-lookup"><span data-stu-id="950c3-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="950c3-112">Pour plus d’informations, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="950c3-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="950c3-113">Arabe (Arabie)</span><span class="sxs-lookup"><span data-stu-id="950c3-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="950c3-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="950c3-114">0x0401</span></span> | <span data-ttu-id="950c3-115">Italien</span><span class="sxs-lookup"><span data-stu-id="950c3-115">Italian</span></span>               | <span data-ttu-id="950c3-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="950c3-116">0x0410</span></span> |
| <span data-ttu-id="950c3-117">Basque</span><span class="sxs-lookup"><span data-stu-id="950c3-117">Basque</span></span>                | <span data-ttu-id="950c3-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="950c3-118">0x042d</span></span> | <span data-ttu-id="950c3-119">Japonais</span><span class="sxs-lookup"><span data-stu-id="950c3-119">Japanese</span></span>              | <span data-ttu-id="950c3-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="950c3-120">0x0411</span></span> |
| <span data-ttu-id="950c3-121">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="950c3-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="950c3-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="950c3-122">0x0804</span></span> | <span data-ttu-id="950c3-123">Coréen</span><span class="sxs-lookup"><span data-stu-id="950c3-123">Korean</span></span>                | <span data-ttu-id="950c3-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="950c3-124">0x0412</span></span> |
| <span data-ttu-id="950c3-125">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="950c3-125">Chinese (Traditional)</span></span> | <span data-ttu-id="950c3-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="950c3-126">0x0404</span></span> | <span data-ttu-id="950c3-127">Norvégien</span><span class="sxs-lookup"><span data-stu-id="950c3-127">Norwegian</span></span>             | <span data-ttu-id="950c3-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="950c3-128">0x0414</span></span> |
| <span data-ttu-id="950c3-129">Croate</span><span class="sxs-lookup"><span data-stu-id="950c3-129">Croatian</span></span>              | <span data-ttu-id="950c3-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="950c3-130">0x041A</span></span> | <span data-ttu-id="950c3-131">Polonais</span><span class="sxs-lookup"><span data-stu-id="950c3-131">Polish</span></span>                | <span data-ttu-id="950c3-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="950c3-132">0x0415</span></span> |
| <span data-ttu-id="950c3-133">Tchèque</span><span class="sxs-lookup"><span data-stu-id="950c3-133">Czech</span></span>                 | <span data-ttu-id="950c3-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="950c3-134">0x0405</span></span> | <span data-ttu-id="950c3-135">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="950c3-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="950c3-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="950c3-136">0x0816</span></span> |
| <span data-ttu-id="950c3-137">Danois</span><span class="sxs-lookup"><span data-stu-id="950c3-137">Danish</span></span>                | <span data-ttu-id="950c3-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="950c3-138">0x0406</span></span> | <span data-ttu-id="950c3-139">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="950c3-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="950c3-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="950c3-140">0x0416</span></span> |
| <span data-ttu-id="950c3-141">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="950c3-141">Dutch</span></span>                 | <span data-ttu-id="950c3-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="950c3-142">0x0413</span></span> | <span data-ttu-id="950c3-143">Roumain</span><span class="sxs-lookup"><span data-stu-id="950c3-143">Romanian</span></span>              | <span data-ttu-id="950c3-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="950c3-144">0x0418</span></span> |
| <span data-ttu-id="950c3-145">Anglais (Royaume-Uni)</span><span class="sxs-lookup"><span data-stu-id="950c3-145">English (British)</span></span>     | <span data-ttu-id="950c3-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="950c3-146">0x0809</span></span> | <span data-ttu-id="950c3-147">Russe</span><span class="sxs-lookup"><span data-stu-id="950c3-147">Russian</span></span>               | <span data-ttu-id="950c3-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="950c3-148">0x0419</span></span> |
| <span data-ttu-id="950c3-149">Anglais (US)</span><span class="sxs-lookup"><span data-stu-id="950c3-149">English (US)</span></span>          | <span data-ttu-id="950c3-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="950c3-150">0x0409</span></span> | <span data-ttu-id="950c3-151">Slovaque</span><span class="sxs-lookup"><span data-stu-id="950c3-151">Slovakian</span></span>             | <span data-ttu-id="950c3-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="950c3-152">0x041B</span></span> |
| <span data-ttu-id="950c3-153">Finnois</span><span class="sxs-lookup"><span data-stu-id="950c3-153">Finnish</span></span>               | <span data-ttu-id="950c3-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="950c3-154">0x040B</span></span> | <span data-ttu-id="950c3-155">Slovène</span><span class="sxs-lookup"><span data-stu-id="950c3-155">Slovenian</span></span>             | <span data-ttu-id="950c3-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="950c3-156">0x0424</span></span> |
| <span data-ttu-id="950c3-157">Français</span><span class="sxs-lookup"><span data-stu-id="950c3-157">French</span></span>                | <span data-ttu-id="950c3-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="950c3-158">0x040C</span></span> | <span data-ttu-id="950c3-159">Espagnol</span><span class="sxs-lookup"><span data-stu-id="950c3-159">Spanish</span></span>               | <span data-ttu-id="950c3-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="950c3-160">0x0C0A</span></span> |
| <span data-ttu-id="950c3-161">Allemand</span><span class="sxs-lookup"><span data-stu-id="950c3-161">German</span></span>                | <span data-ttu-id="950c3-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="950c3-162">0x0407</span></span> | <span data-ttu-id="950c3-163">Suédois</span><span class="sxs-lookup"><span data-stu-id="950c3-163">Swedish</span></span>               | <span data-ttu-id="950c3-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="950c3-164">0x041D</span></span> |
| <span data-ttu-id="950c3-165">Grec</span><span class="sxs-lookup"><span data-stu-id="950c3-165">Greek</span></span>                 | <span data-ttu-id="950c3-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="950c3-166">0x0408</span></span> | <span data-ttu-id="950c3-167">Thaï</span><span class="sxs-lookup"><span data-stu-id="950c3-167">Thai</span></span>                  | <span data-ttu-id="950c3-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="950c3-168">0x041E</span></span> |
| <span data-ttu-id="950c3-169">Hébreu</span><span class="sxs-lookup"><span data-stu-id="950c3-169">Hebrew</span></span>                | <span data-ttu-id="950c3-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="950c3-170">0x040D</span></span> | <span data-ttu-id="950c3-171">Turc</span><span class="sxs-lookup"><span data-stu-id="950c3-171">Turkish</span></span>               | <span data-ttu-id="950c3-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="950c3-172">0x041F</span></span> |
| <span data-ttu-id="950c3-173">Hongrois</span><span class="sxs-lookup"><span data-stu-id="950c3-173">Hungarian</span></span>             | <span data-ttu-id="950c3-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="950c3-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="950c3-175">Si vous ne définissez pas l’ID de langue pour le caractère, son ID de langue sera l’ID de langue actuel du système si la DLL de langue de l’agent correspondante est installée. dans le cas contraire, la langue du caractère sera l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="950c3-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="950c3-176">Cette propriété détermine également la langue du texte de la bulle, les commandes du menu contextuel du caractère et le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="950c3-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="950c3-177">Elle détermine également la langue par défaut de la sortie TTS.</span><span class="sxs-lookup"><span data-stu-id="950c3-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="950c3-178">Pour déterminer si un moteur vocal compatible est disponible pour la langue du caractère, utilisez [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="950c3-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="950c3-179">Si vous essayez de définir l’ID de langue d’un caractère et les ressources linguistiques de l’agent, la page de codes ou une police d’affichage pour l’ID de langue n’est pas disponible, l’agent retourne une erreur et l’ID de langue du caractère reste le dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="950c3-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="950c3-180">La définition de cette propriété ne retourne pas d’erreur s’il n’existe aucun moteur de reconnaissance vocale correspondant à la langue.</span><span class="sxs-lookup"><span data-stu-id="950c3-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="950c3-181">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="950c3-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="950c3-182">Si vous définissez l’ID de langue du caractère sur une langue qui prend en charge le texte bidirectionnel (tel que l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle installée, le texte apparaît dans le mot-bulle dans l’ordre logique plutôt que dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="950c3-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="950c3-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="950c3-183">See Also</span></span>

<span data-ttu-id="950c3-184">[**IAgentCharacterEx : GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx :: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx :: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="950c3-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




