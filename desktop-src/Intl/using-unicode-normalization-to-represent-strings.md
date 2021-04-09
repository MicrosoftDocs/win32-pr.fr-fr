---
description: Les applications peuvent utiliser Unicode pour représenter des chaînes dans plusieurs formulaires.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Utilisation de la normalisation Unicode pour représenter des chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869073"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="b662f-103">Utilisation de la normalisation Unicode pour représenter des chaînes</span><span class="sxs-lookup"><span data-stu-id="b662f-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="b662f-104">Les applications peuvent utiliser Unicode pour représenter des chaînes dans plusieurs formulaires.</span><span class="sxs-lookup"><span data-stu-id="b662f-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="b662f-105">Au fur et à mesure de l’augmentation de l’acceptation Unicode, en particulier via Internet, le besoin est venu d’éliminer les différences non essentielles dans les chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="b662f-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="b662f-106">Plusieurs représentations pour une combinaison de caractères compliquent le logiciel, par exemple, lorsqu’un serveur Web répond à une demande de page ou lorsqu’un éditeur de liens recherche un identificateur particulier dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b662f-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="b662f-107">Différentes chaînes Unicode peuvent sembler identiques visuellement, ce qui soulève des problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b662f-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="b662f-108">Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="b662f-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="b662f-109">En réponse à cette exigence, le consortium Unicode a défini un processus appelé « normalisation », qui produit une représentation binaire pour toute représentation binaire équivalente d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="b662f-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="b662f-110">Une fois normalisé, deux chaînes sont équivalentes si et seulement si elles ont des représentations binaires identiques.</span><span class="sxs-lookup"><span data-stu-id="b662f-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="b662f-111">La normalisation élimine certaines différences, mais conserve la casse.</span><span class="sxs-lookup"><span data-stu-id="b662f-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="b662f-112">Pour utiliser la normalisation Unicode, une application peut appeler les fonctions [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) et [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) pour la réorganisation des chaînes microsoft au format Unicode 4,0 tr \# 15.</span><span class="sxs-lookup"><span data-stu-id="b662f-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="b662f-113">La normalisation peut contribuer à améliorer la sécurité en réduisant les autres représentations de chaîne qui ont la même signification linguistique.</span><span class="sxs-lookup"><span data-stu-id="b662f-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="b662f-114">N’oubliez pas, cependant, que la normalisation ne peut pas éliminer entièrement d’autres représentations.</span><span class="sxs-lookup"><span data-stu-id="b662f-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="b662f-115">Pour obtenir une description détaillée des normes Unicode pour la normalisation, reportez-vous à la [norme Unicode annexe \# 15 : formulaires de normalisation Unicode](https://www.unicode.org/reports/tr15) (uax \# 15).</span><span class="sxs-lookup"><span data-stu-id="b662f-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="b662f-116">Étant donné que la normalisation peut modifier la forme d’une chaîne, les mécanismes de sécurité ou les algorithmes de validation de caractères doivent généralement être implémentés après la normalisation.</span><span class="sxs-lookup"><span data-stu-id="b662f-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="b662f-117">Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="b662f-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="b662f-118">Fournir plusieurs représentations de la même chaîne</span><span class="sxs-lookup"><span data-stu-id="b662f-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="b662f-119">Dans de nombreux cas, Unicode autorise plusieurs représentations de ce qui est, linguistiquement, de la même chaîne.</span><span class="sxs-lookup"><span data-stu-id="b662f-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="b662f-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b662f-120">For example:</span></span>

-   <span data-ttu-id="b662f-121">Le capital A avec ditréma (tréma) peut être représenté comme un seul point de code Unicode « Ä » (U + 00C4) ou la combinaison du capital A et du caractère ditréma (« A » + « ̈ », c’est-à-dire U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="b662f-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="b662f-122">Des considérations similaires s’appliquent à de nombreux autres caractères avec des marques diacritiques.</span><span class="sxs-lookup"><span data-stu-id="b662f-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="b662f-123">Le capital A lui-même peut être représenté de la manière habituelle (lettre majuscule latine A, U + 0041) ou par la lettre majuscule latine A pleine chasse (U + FF21).</span><span class="sxs-lookup"><span data-stu-id="b662f-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="b662f-124">Des considérations similaires s’appliquent aux autres lettres latines simples (majuscules et minuscules) et aux caractères katakana utilisés lors de l’écriture du japonais.</span><span class="sxs-lookup"><span data-stu-id="b662f-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="b662f-125">La chaîne « fi » peut être représentée par les caractères « f » et « i » (U + 0066 U + 0069) ou par la ligature « fi » (U + FB01).</span><span class="sxs-lookup"><span data-stu-id="b662f-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="b662f-126">Des considérations similaires s’appliquent à de nombreuses autres combinaisons de caractères pour lesquelles Unicode définit des ligatures.</span><span class="sxs-lookup"><span data-stu-id="b662f-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="b662f-127">Utiliser les quatre formulaires de normalisation définis</span><span class="sxs-lookup"><span data-stu-id="b662f-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="b662f-128">Vos applications peuvent effectuer une normalisation Unicode à l’aide de plusieurs algorithmes, appelés « formulaires de normalisation », qui obéissent à différentes règles.</span><span class="sxs-lookup"><span data-stu-id="b662f-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="b662f-129">Le consortium Unicode a défini quatre formulaires de normalisation : NFC (Form C), NFD (Form D), NFKC (Form KC) et NFKD (Form KD).</span><span class="sxs-lookup"><span data-stu-id="b662f-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="b662f-130">Chaque formulaire élimine quelques différences, mais conserve la casse.</span><span class="sxs-lookup"><span data-stu-id="b662f-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="b662f-131">Win32 et le .NET Framework prennent en charge les quatre formulaires de normalisation.</span><span class="sxs-lookup"><span data-stu-id="b662f-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="b662f-132">La [**\_ forme**](/windows/desktop/api/Winnls/ne-winnls-norm_form) normale de type énumération nls prend en charge les quatre formulaires standard de normalisation Unicode.</span><span class="sxs-lookup"><span data-stu-id="b662f-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="b662f-133">Les formulaires C et D fournissent des formes canoniques pour les chaînes.</span><span class="sxs-lookup"><span data-stu-id="b662f-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="b662f-134">Les formes non canoniques KC et KD offrent une meilleure compatibilité et peuvent révéler certaines équivalences sémantiques qui ne sont pas visibles dans les formulaires C et D. Toutefois, ils le font au détriment d’une certaine perte d’informations et ne doivent généralement pas être utilisés comme un moyen canonique de stocker des chaînes.</span><span class="sxs-lookup"><span data-stu-id="b662f-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="b662f-135">Parmi les deux formes canoniques, le formulaire C est un formulaire « composé » et le formulaire D est un formulaire « décomposé ».</span><span class="sxs-lookup"><span data-stu-id="b662f-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="b662f-136">Par exemple, le formulaire C utilise le point de code Unicode unique « Ä » (U + 00C4), tandis que le format D utilise (« A » + « ̈ », c’est-à-dire U + 0041 U + 0308).</span><span class="sxs-lookup"><span data-stu-id="b662f-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="b662f-137">Elles s’affichent de la même façon, car « ̈ » (U + 0308) est un caractère d’association.</span><span class="sxs-lookup"><span data-stu-id="b662f-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="b662f-138">Le formulaire D peut utiliser un nombre quelconque de points de code pour représenter un point de code unique utilisé par le formulaire C.</span><span class="sxs-lookup"><span data-stu-id="b662f-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="b662f-139">Si deux chaînes sont identiques au format C ou au format D, elles sont identiques dans l’autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="b662f-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="b662f-140">En outre, lorsqu’elles sont correctement rendues, elles s’affichent de façon indifférenciée les unes des autres et de la chaîne non normalisée d’origine.</span><span class="sxs-lookup"><span data-stu-id="b662f-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="b662f-141">Une fois normalisés, les chaînes ne peuvent pas être retournées de façon cohérente à leur représentation d’origine.</span><span class="sxs-lookup"><span data-stu-id="b662f-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="b662f-142">Par exemple, si une chaîne avec un mélange de représentations de caractères composés et décomposées est convertie en une forme normalisée, il n’existe aucun moyen de la dénormaliser dans la chaîne mixte d’origine.</span><span class="sxs-lookup"><span data-stu-id="b662f-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="b662f-143">Par conséquent, si une application requiert la représentation d’origine de la chaîne, elle doit stocker cette représentation explicitement.</span><span class="sxs-lookup"><span data-stu-id="b662f-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="b662f-144">Toutefois, la conversion entre les deux formes canoniques est réversible.</span><span class="sxs-lookup"><span data-stu-id="b662f-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="b662f-145">Une chaîne dans le formulaire C peut être convertie au format D, puis revers le formulaire C, et le résultat est identique à la chaîne C du formulaire d’origine.</span><span class="sxs-lookup"><span data-stu-id="b662f-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="b662f-146">Les formulaires KC et KD sont similaires aux formulaires C et D, respectivement, mais ces « formulaires de compatibilité » comportent des mappages supplémentaires de caractères compatibles avec la forme de base de chaque caractère.</span><span class="sxs-lookup"><span data-stu-id="b662f-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="b662f-147">De tels mappages peuvent entraîner la perte de modifications de caractères mineurs.</span><span class="sxs-lookup"><span data-stu-id="b662f-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="b662f-148">Ils combinent certains caractères qui sont visuellement distincts.</span><span class="sxs-lookup"><span data-stu-id="b662f-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="b662f-149">Par exemple, ils combinent des caractères à pleine chasse et demi-chasse avec la même signification sémantique, ou différentes formes de la même lettre arabe, ou la ligature « fi » (U + FB01) et la paire de caractères « fi » (U + 0066 U + 0069).</span><span class="sxs-lookup"><span data-stu-id="b662f-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="b662f-150">Ils combinent également certains caractères qui peuvent parfois avoir une signification sémantique différente, par exemple un chiffre écrit sous la forme d’un exposant, sous la forme d’un indice ou placé dans un cercle.</span><span class="sxs-lookup"><span data-stu-id="b662f-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="b662f-151">En raison de cette perte d’informations, les formulaires KC et KD ne doivent généralement pas être utilisés comme formes canoniques de chaînes, mais ils sont utiles pour certaines applications.</span><span class="sxs-lookup"><span data-stu-id="b662f-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="b662f-152">Le formulaire KC est un formulaire composé et le formulaire KD est un formulaire décomposé.</span><span class="sxs-lookup"><span data-stu-id="b662f-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="b662f-153">L’application peut basculer entre les formulaires KC et KD, mais il n’existe pas de méthode cohérente pour revenir de la forme KC ou KD à la chaîne d’origine, même si la chaîne d’origine est au format C ou D.</span><span class="sxs-lookup"><span data-stu-id="b662f-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="b662f-154">Windows, les applications Microsoft et le .NET Framework génèrent généralement des caractères au format C à l’aide de méthodes d’entrée normales.</span><span class="sxs-lookup"><span data-stu-id="b662f-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="b662f-155">Pour la plupart des cas sur Windows, le formulaire C est le formulaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="b662f-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="b662f-156">Par exemple, les caractères du formulaire C sont générés par l’entrée clavier Windows.</span><span class="sxs-lookup"><span data-stu-id="b662f-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="b662f-157">Toutefois, les caractères importés à partir du Web et d’autres plateformes peuvent introduire d’autres formulaires de normalisation dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="b662f-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="b662f-158">Les exemples suivants sont tirés de UAX \# 15 et illustrent les différences entre les quatre formulaires de normalisation.</span><span class="sxs-lookup"><span data-stu-id="b662f-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b662f-159">Original</span><span class="sxs-lookup"><span data-stu-id="b662f-159">Original</span></span></th>
<th><span data-ttu-id="b662f-160">Formulaire D</span><span class="sxs-lookup"><span data-stu-id="b662f-160">Form D</span></span></th>
<th><span data-ttu-id="b662f-161">Formulaire C</span><span class="sxs-lookup"><span data-stu-id="b662f-161">Form C</span></span></th>
<th><span data-ttu-id="b662f-162">Notes</span><span class="sxs-lookup"><span data-stu-id="b662f-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b662f-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="b662f-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="b662f-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="b662f-166">La ffi_ligature (U + FB03) n’est pas décomposée, car elle a un mappage de compatibilité, et non un mappage canonique. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="b662f-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="b662f-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="b662f-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="b662f-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="b662f-173">Le chiffre romain IV (U + 2163) n’est pas décomposé. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="b662f-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="b662f-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-177">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-177">ga</span></span></td>
<td><span data-ttu-id="b662f-178">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-178">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-179">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="b662f-180">Les équivalents de compatibilité différents d’un caractère japonais unique n’entraînent pas la même chaîne au format C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-181">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-181">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-182">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-182">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-183">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b662f-187">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-188">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-189">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-190">hw_ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="b662f-191">hw_ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="b662f-192">hw_ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b662f-193">kaks</span><span class="sxs-lookup"><span data-stu-id="b662f-193">kaks</span></span></td>
<td><span data-ttu-id="b662f-194">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="b662f-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="b662f-195">kaks</span><span class="sxs-lookup"><span data-stu-id="b662f-195">kaks</span></span></td>
<td><span data-ttu-id="b662f-196">Les syllabes Hangul sont conservées dans une normalisation.</span><span class="sxs-lookup"><span data-stu-id="b662f-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b662f-197">Original</span><span class="sxs-lookup"><span data-stu-id="b662f-197">Original</span></span></th>
<th><span data-ttu-id="b662f-198">Forme KD</span><span class="sxs-lookup"><span data-stu-id="b662f-198">Form KD</span></span></th>
<th><span data-ttu-id="b662f-199">Forme KC</span><span class="sxs-lookup"><span data-stu-id="b662f-199">Form KC</span></span></th>
<th><span data-ttu-id="b662f-200">Notes</span><span class="sxs-lookup"><span data-stu-id="b662f-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b662f-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="b662f-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="b662f-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="b662f-204">Le ffi_ligature (U + FB03) est décomposé sous forme KC, mais pas dans le formulaire C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="b662f-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="b662f-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="b662f-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="b662f-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="b662f-211">Les chaînes résultantes sont identiques sous la forme KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="b662f-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="b662f-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="b662f-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-215">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-215">ga</span></span></td>
<td><span data-ttu-id="b662f-216">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-216">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-217">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="b662f-218">Différents équivalents de compatibilité d’un caractère japonais unique génèrent la même chaîne sous la forme KC. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b662f-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b662f-219">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-219">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-220">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-220">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-221">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-223">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-223">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-224">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b662f-225">Ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="b662f-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="b662f-226">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-226">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-227">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b662f-228">hw_ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="b662f-229">Ka + dix</span><span class="sxs-lookup"><span data-stu-id="b662f-229">ka +ten</span></span></td>
<td><span data-ttu-id="b662f-230">ga</span><span class="sxs-lookup"><span data-stu-id="b662f-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b662f-231">kaks</span><span class="sxs-lookup"><span data-stu-id="b662f-231">kaks</span></span></td>
<td><span data-ttu-id="b662f-232">k <sub>i</sub> + a m + KS <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="b662f-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="b662f-233">kaks</span><span class="sxs-lookup"><span data-stu-id="b662f-233">kaks</span></span></td>
<td><span data-ttu-id="b662f-234">Les syllabes Hangul sont conservées dans une normalisation.</span><span class="sxs-lookup"><span data-stu-id="b662f-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="b662f-235">Dans les versions Unicode antérieures, les caractères Jamos comme KS <sub>f</sub> avaient des mappages de compatibilité à k <sub>f</sub> + s <sub>f</sub>.</span><span class="sxs-lookup"><span data-stu-id="b662f-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="b662f-236">Ces mappages ont été supprimés dans les 2.1.9 Unicode pour garantir le maintien des syllabes Hangul.</span><span class="sxs-lookup"><span data-stu-id="b662f-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="b662f-237">Les deux tableaux ci-dessus ont un copyright de © 1998-2006 Unicode, Inc. Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="b662f-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="b662f-238">Utiliser des formulaires composés pour des glyphes uniques</span><span class="sxs-lookup"><span data-stu-id="b662f-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="b662f-239">De nombreuses séquences de caractères qui correspondent à un seul glyphe n’ont pas de formes composées.</span><span class="sxs-lookup"><span data-stu-id="b662f-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="b662f-240">Même en cas de normalisation par le formulaire C, un seul élément de texte logique ou de glyphe visuel peut être composé de plusieurs points de code Unicode.</span><span class="sxs-lookup"><span data-stu-id="b662f-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="b662f-241">Par exemple, plusieurs caractères utilisés pour écrire du lituanien ont des signes diacritiques doubles, car ils ont uniquement des formulaires décomposés.</span><span class="sxs-lookup"><span data-stu-id="b662f-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="b662f-242">Par exemple, U minuscule avec macron et tilde ("ū̃", U + 016b U + 0303, où le premier point de code est un U minuscule avec macron et le second est un accent aigu de combinaison).</span><span class="sxs-lookup"><span data-stu-id="b662f-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="b662f-243">Exemple</span><span class="sxs-lookup"><span data-stu-id="b662f-243">Example</span></span>

<span data-ttu-id="b662f-244">Un exemple pertinent se trouve dans l' [exemple nls : Unicode Normalization](nls--unicode-normalization-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b662f-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b662f-245">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b662f-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b662f-246">Utilisation de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="b662f-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b662f-247">Considérations relatives à la sécurité : fonctionnalités internationales</span><span class="sxs-lookup"><span data-stu-id="b662f-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="b662f-248">**IsNormalizedString**</span><span class="sxs-lookup"><span data-stu-id="b662f-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="b662f-249">**NormalizeString**</span><span class="sxs-lookup"><span data-stu-id="b662f-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




