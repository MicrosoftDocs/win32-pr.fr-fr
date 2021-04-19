---
description: L’arabe et de nombreuses autres langues ont des formes classiques pour les nombres qui diffèrent des chiffres occidentaux conventionnels les plus souvent utilisés sur les ordinateurs.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formes de chiffres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523384"
---
# <a name="digit-shapes"></a><span data-ttu-id="6965c-103">Formes de chiffres</span><span class="sxs-lookup"><span data-stu-id="6965c-103">Digit Shapes</span></span>

<span data-ttu-id="6965c-104">L’arabe et de nombreuses autres langues ont des formes classiques pour les nombres qui diffèrent des chiffres occidentaux conventionnels les plus souvent utilisés sur les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6965c-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="6965c-105">Pour éviter toute ambiguïté lors de l’attribution d’un nom à ces formes, ce document utilise les noms suivants de la norme Unicode.</span><span class="sxs-lookup"><span data-stu-id="6965c-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="6965c-106">Nom Unicode des chiffres</span><span class="sxs-lookup"><span data-stu-id="6965c-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="6965c-107">Pays/région utilisé (e)</span><span class="sxs-lookup"><span data-stu-id="6965c-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6965c-108">Chiffres européens</span><span class="sxs-lookup"><span data-stu-id="6965c-108">European digits</span></span>                                                | <span data-ttu-id="6965c-109">Europe, Amérique et dans de nombreux autres pays/régions</span><span class="sxs-lookup"><span data-stu-id="6965c-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="6965c-110">Chiffres Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="6965c-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="6965c-111">Pays/régions arabes (bien que beaucoup utilisent des chiffres européens)</span><span class="sxs-lookup"><span data-stu-id="6965c-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="6965c-112">Autres chiffres nationaux : chiffres indo-aryens, chiffres thaïs et similaires</span><span class="sxs-lookup"><span data-stu-id="6965c-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="6965c-113">Différents pays/régions</span><span class="sxs-lookup"><span data-stu-id="6965c-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="6965c-114">Unicode fournit des points de code distincts pour chaque forme de chiffre.</span><span class="sxs-lookup"><span data-stu-id="6965c-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="6965c-115">Ainsi, pour accéder à des formes de chiffres de langue spéciales, votre application peut utiliser les codes de caractères Unicode appropriés pour les chiffres ci-dessus, U + 0030 à U + 0039.</span><span class="sxs-lookup"><span data-stu-id="6965c-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="6965c-116">Ces codes sont toujours affichés avec la forme appropriée, selon la disponibilité de la police.</span><span class="sxs-lookup"><span data-stu-id="6965c-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="6965c-117">Les codes de caractères Unicode U + 0030 à U + 0039 représentent les chiffres européens de 0 à 9, mais leur forme de chiffres peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="6965c-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="6965c-118">Les API de texte GDI et DirectWrite fournissent des mécanismes permettant aux applications de contrôler ce comportement.</span><span class="sxs-lookup"><span data-stu-id="6965c-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="6965c-119">(Voir, par exemple, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) ou [**IDWriteTextAnalysisSink :: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) Le comportement dans certains contrôles de l’interpréteur de commandes et les infrastructures d’interface utilisateur peut répondre aux paramètres régionaux de l’utilisateur pour la substitution de chiffres ; les paramètres [régionaux \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE peuvent être utilisés pour obtenir les paramètres de substitution de chiffres par défaut pour différents paramètres régionaux ou les paramètres de bureau de l’utilisateur actuel pour la substitution de chiffres.</span><span class="sxs-lookup"><span data-stu-id="6965c-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="6965c-120">Chiffres natifs</span><span class="sxs-lookup"><span data-stu-id="6965c-120">Native Digits</span></span>

<span data-ttu-id="6965c-121">Les chiffres natifs sont les formes de chiffres choisies par l’utilisateur dans la feuille de propriétés **nombre** dans la partie Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="6965c-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="6965c-122">Pour trouver la présentation de chiffres préférée par l’utilisateur, votre application utilise la fonction [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante [ \_ SNATIVEDIGITS locale](locale-snative-constants.md) qui représente les informations de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="6965c-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="6965c-123">En règle générale, les codes numériques Unicode sont générés dans les routines du système d’exploitation du Runtime.</span><span class="sxs-lookup"><span data-stu-id="6965c-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="6965c-124">Par conséquent, les systèmes d’exploitation Common Runtime doivent être mis à niveau pour que l’application inspecte les [paramètres régionaux \_ SNATIVEDIGITS](locale-snative-constants.md) de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="6965c-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="6965c-125">Substitution de chiffres</span><span class="sxs-lookup"><span data-stu-id="6965c-125">Digit Substitution</span></span>

<span data-ttu-id="6965c-126">L’application peut utiliser la substitution de chiffres pour indiquer au système d’exploitation comment imprimer les chiffres U + 0030 à U + 0039.</span><span class="sxs-lookup"><span data-stu-id="6965c-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="6965c-127">La constante [ \_ IDIGITSUBSTITUTION de paramètres régionaux](locale-idigitsubstitution.md) contrôle cette opération.</span><span class="sxs-lookup"><span data-stu-id="6965c-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="6965c-128">Mise en forme des chiffres pour une fonction unique</span><span class="sxs-lookup"><span data-stu-id="6965c-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="6965c-129">Les fonctions de [ \_ résultats](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)et GCP ont des indicateurs qui régissent la substitution des codes Unicode U + 0030 à u + 0039 pour la durée de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="6965c-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="6965c-130">Ces indicateurs remplacent les paramètres régionaux dans le panneau de configuration, mais ne réinitialisent pas les paramètres.</span><span class="sxs-lookup"><span data-stu-id="6965c-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="6965c-131">En outre, ils ne remplacent pas les codes Unicode NADS et nœuds.</span><span class="sxs-lookup"><span data-stu-id="6965c-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="6965c-132">Les indicateurs suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="6965c-132">The following flags are available.</span></span>



| <span data-ttu-id="6965c-133">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="6965c-133">Flags</span></span>                 | <span data-ttu-id="6965c-134">Chiffres utilisés</span><span class="sxs-lookup"><span data-stu-id="6965c-134">Digits used</span></span>                      | <span data-ttu-id="6965c-135">Utilisé dans</span><span class="sxs-lookup"><span data-stu-id="6965c-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="6965c-136">\_NUMERICSLATIN ETO</span><span class="sxs-lookup"><span data-stu-id="6965c-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="6965c-137">Chiffres européens</span><span class="sxs-lookup"><span data-stu-id="6965c-137">European digits</span></span>                  | <span data-ttu-id="6965c-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="6965c-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="6965c-139">\_NUMERICSLOCAL ETO</span><span class="sxs-lookup"><span data-stu-id="6965c-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="6965c-140">Chiffres appropriés aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="6965c-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="6965c-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="6965c-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="6965c-142">GCP \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="6965c-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="6965c-143">Chiffres européens</span><span class="sxs-lookup"><span data-stu-id="6965c-143">European digits</span></span>                  | <span data-ttu-id="6965c-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="6965c-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="6965c-145">GCP \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="6965c-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="6965c-146">Chiffres appropriés aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="6965c-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="6965c-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="6965c-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="6965c-148">GCPCLASS \_ LATINNUMBER</span><span class="sxs-lookup"><span data-stu-id="6965c-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="6965c-149">Chiffres européens</span><span class="sxs-lookup"><span data-stu-id="6965c-149">European digits</span></span>                  | <span data-ttu-id="6965c-150">**résultats de GCP \_**</span><span class="sxs-lookup"><span data-stu-id="6965c-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="6965c-151">GCPCLASS \_ LOCALNUMBER</span><span class="sxs-lookup"><span data-stu-id="6965c-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="6965c-152">Chiffres appropriés aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="6965c-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="6965c-153">**résultats de GCP \_**</span><span class="sxs-lookup"><span data-stu-id="6965c-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="6965c-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6965c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6965c-155">À propos de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="6965c-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6965c-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="6965c-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="6965c-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="6965c-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
