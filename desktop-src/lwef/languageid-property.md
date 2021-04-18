---
title: LanguageID, propriété
description: LanguageID, propriété
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311038"
---
# <a name="languageid-property"></a><span data-ttu-id="e2be3-103">LanguageID, propriété</span><span class="sxs-lookup"><span data-stu-id="e2be3-103">LanguageID Property</span></span>

<span data-ttu-id="e2be3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2be3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e2be3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="e2be3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e2be3-106">Retourne ou définit l’ID de langue pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="e2be3-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="e2be3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="e2be3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e2be3-108">Caractères agent. \*\* \*\* \*  \* **(«***CharacterID***»).** \[  =  *LanguageID* LanguageID\]</span><span class="sxs-lookup"><span data-stu-id="e2be3-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="e2be3-109">Partie</span><span class="sxs-lookup"><span data-stu-id="e2be3-109">Part</span></span>

<span data-ttu-id="e2be3-110">Description</span><span class="sxs-lookup"><span data-stu-id="e2be3-110">Description</span></span>

<span data-ttu-id="e2be3-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="e2be3-111">LanguageID</span></span>

<span data-ttu-id="e2be3-112">Entier long spécifiant l’ID de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="e2be3-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="e2be3-113">L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="e2be3-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="e2be3-114">Les exemples suivants sont des valeurs pour les langues prises en charge par Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e2be3-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="e2be3-115">Pour déterminer la valeur d’autres langages, consultez la *documentation du kit de développement Platform SDK*.</span><span class="sxs-lookup"><span data-stu-id="e2be3-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="e2be3-116">Arabe</span><span class="sxs-lookup"><span data-stu-id="e2be3-116">Arabic</span></span>

<span data-ttu-id="e2be3-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="e2be3-117">&H0401</span></span>

<span data-ttu-id="e2be3-118">Italien</span><span class="sxs-lookup"><span data-stu-id="e2be3-118">Italian</span></span>

<span data-ttu-id="e2be3-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="e2be3-119">&H0410</span></span>

 

<span data-ttu-id="e2be3-120">Basque</span><span class="sxs-lookup"><span data-stu-id="e2be3-120">Basque</span></span>

<span data-ttu-id="e2be3-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="e2be3-121">&H042D</span></span>

<span data-ttu-id="e2be3-122">Japonais</span><span class="sxs-lookup"><span data-stu-id="e2be3-122">Japanese</span></span>

<span data-ttu-id="e2be3-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="e2be3-123">&H0411</span></span>

 

<span data-ttu-id="e2be3-124">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="e2be3-124">Chinese (Simplified)</span></span>

<span data-ttu-id="e2be3-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="e2be3-125">&H0804</span></span>

<span data-ttu-id="e2be3-126">Coréen</span><span class="sxs-lookup"><span data-stu-id="e2be3-126">Korean</span></span>

<span data-ttu-id="e2be3-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="e2be3-127">&H0412</span></span>

 

<span data-ttu-id="e2be3-128">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="e2be3-128">Chinese (Traditional)</span></span>

<span data-ttu-id="e2be3-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="e2be3-129">&H0404</span></span>

<span data-ttu-id="e2be3-130">Norvégien</span><span class="sxs-lookup"><span data-stu-id="e2be3-130">Norwegian</span></span>

<span data-ttu-id="e2be3-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="e2be3-131">&H0414</span></span>

 

<span data-ttu-id="e2be3-132">Croate</span><span class="sxs-lookup"><span data-stu-id="e2be3-132">Croatian</span></span>

<span data-ttu-id="e2be3-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="e2be3-133">&H041A</span></span>

<span data-ttu-id="e2be3-134">Polonais</span><span class="sxs-lookup"><span data-stu-id="e2be3-134">Polish</span></span>

<span data-ttu-id="e2be3-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="e2be3-135">&H0415</span></span>

 

<span data-ttu-id="e2be3-136">Tchèque</span><span class="sxs-lookup"><span data-stu-id="e2be3-136">Czech</span></span>

<span data-ttu-id="e2be3-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="e2be3-137">&H0405</span></span>

<span data-ttu-id="e2be3-138">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="e2be3-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="e2be3-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="e2be3-139">&H0816</span></span>

 

<span data-ttu-id="e2be3-140">Danois</span><span class="sxs-lookup"><span data-stu-id="e2be3-140">Danish</span></span>

<span data-ttu-id="e2be3-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="e2be3-141">&H0406</span></span>

<span data-ttu-id="e2be3-142">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="e2be3-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="e2be3-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="e2be3-143">&H0416</span></span>

 

<span data-ttu-id="e2be3-144">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="e2be3-144">Dutch</span></span>

<span data-ttu-id="e2be3-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="e2be3-145">&H0413</span></span>

<span data-ttu-id="e2be3-146">Roumain</span><span class="sxs-lookup"><span data-stu-id="e2be3-146">Romanian</span></span>

<span data-ttu-id="e2be3-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="e2be3-147">&H0418</span></span>

 

<span data-ttu-id="e2be3-148">Anglais (Royaume-Uni)</span><span class="sxs-lookup"><span data-stu-id="e2be3-148">English (British)</span></span>

<span data-ttu-id="e2be3-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="e2be3-149">&H0809</span></span>

<span data-ttu-id="e2be3-150">Russe</span><span class="sxs-lookup"><span data-stu-id="e2be3-150">Russian</span></span>

<span data-ttu-id="e2be3-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="e2be3-151">&H0419</span></span>

 

<span data-ttu-id="e2be3-152">Anglais (US)</span><span class="sxs-lookup"><span data-stu-id="e2be3-152">English (US)</span></span>

<span data-ttu-id="e2be3-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="e2be3-153">&H0409</span></span>

<span data-ttu-id="e2be3-154">Slovaque</span><span class="sxs-lookup"><span data-stu-id="e2be3-154">Slovakian</span></span>

<span data-ttu-id="e2be3-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="e2be3-155">&H041B</span></span>

 

<span data-ttu-id="e2be3-156">Finnois</span><span class="sxs-lookup"><span data-stu-id="e2be3-156">Finnish</span></span>

<span data-ttu-id="e2be3-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="e2be3-157">&H040B</span></span>

<span data-ttu-id="e2be3-158">Slovène</span><span class="sxs-lookup"><span data-stu-id="e2be3-158">Slovenian</span></span>

<span data-ttu-id="e2be3-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="e2be3-159">&H0424</span></span>

 

<span data-ttu-id="e2be3-160">Français</span><span class="sxs-lookup"><span data-stu-id="e2be3-160">French</span></span>

<span data-ttu-id="e2be3-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="e2be3-161">&H040C</span></span>

<span data-ttu-id="e2be3-162">Espagnol</span><span class="sxs-lookup"><span data-stu-id="e2be3-162">Spanish</span></span>

<span data-ttu-id="e2be3-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="e2be3-163">&H0C0A</span></span>

 

<span data-ttu-id="e2be3-164">Allemand</span><span class="sxs-lookup"><span data-stu-id="e2be3-164">German</span></span>

<span data-ttu-id="e2be3-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="e2be3-165">&H0407</span></span>

<span data-ttu-id="e2be3-166">Suédois</span><span class="sxs-lookup"><span data-stu-id="e2be3-166">Swedish</span></span>

<span data-ttu-id="e2be3-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="e2be3-167">&H041D</span></span>

 

<span data-ttu-id="e2be3-168">Grec</span><span class="sxs-lookup"><span data-stu-id="e2be3-168">Greek</span></span>

<span data-ttu-id="e2be3-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="e2be3-169">&H0408</span></span>

<span data-ttu-id="e2be3-170">Thaï</span><span class="sxs-lookup"><span data-stu-id="e2be3-170">Thai</span></span>

<span data-ttu-id="e2be3-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="e2be3-171">&H041E</span></span>

 

<span data-ttu-id="e2be3-172">Hébreu</span><span class="sxs-lookup"><span data-stu-id="e2be3-172">Hebrew</span></span>

<span data-ttu-id="e2be3-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="e2be3-173">&H040D</span></span>

<span data-ttu-id="e2be3-174">Turc</span><span class="sxs-lookup"><span data-stu-id="e2be3-174">Turkish</span></span>

<span data-ttu-id="e2be3-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="e2be3-175">&H041F</span></span>

 

<span data-ttu-id="e2be3-176">Hongrois</span><span class="sxs-lookup"><span data-stu-id="e2be3-176">Hungarian</span></span>

<span data-ttu-id="e2be3-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="e2be3-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2be3-178">Notes</span><span class="sxs-lookup"><span data-stu-id="e2be3-178">Remarks</span></span>

<span data-ttu-id="e2be3-179">Si vous ne définissez pas l' **LanguageID** pour le caractère, son ID de langue sera l’ID de langue du système actuel si la dll de langue de l’agent correspondante est installée ; sinon, la langue du caractère sera l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="e2be3-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="e2be3-180">Cette propriété détermine également la langue du texte de l’info-bulle, les commandes du menu contextuel du caractère et le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="e2be3-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="e2be3-181">Elle détermine également la langue par défaut de la sortie TTS.</span><span class="sxs-lookup"><span data-stu-id="e2be3-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="e2be3-182">Si vous essayez de définir **LanguageID** pour un caractère et que la dll de langue de l’agent pour cette langue n’est pas installée ou qu’une police d’affichage pour l’ID de langue n’est pas disponible, l’agent génère une erreur et **LanguageID** conserve son dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="e2be3-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="e2be3-183">La définition de cette propriété ne déclenche pas d’erreur s’il n’existe aucun moteur de reconnaissance vocale correspondant à la langue.</span><span class="sxs-lookup"><span data-stu-id="e2be3-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="e2be3-184">Pour déterminer si un moteur vocal compatible est disponible pour **LanguageID**, vérifiez [**SRModeID**](srmodeid-property.md) ou [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="e2be3-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="e2be3-185">Si vous ne définissez pas **LanguageID**, il sera défini sur le paramètre ID de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2be3-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="e2be3-186">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="e2be3-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e2be3-187">Si vous affectez à **LanguageID** une langue qui prend en charge le texte bidirectionnel (tel que l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle, le texte de la bulle est affiché dans l’ordre logique plutôt que dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e2be3-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e2be3-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2be3-188">See Also</span></span>

<span data-ttu-id="e2be3-189">[**Propriété SRModeID**](srmodeid-property.md), [ **propriété TTSModeID**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="e2be3-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




