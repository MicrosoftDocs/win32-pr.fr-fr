---
description: Définit des valeurs de chaîne constantes qui sont utilisées pour augmenter la précision de la reconnaissance en fournissant des informations contextuelles au module de reconnaissance.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes Factoid (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526595"
---
# <a name="factoid-constants"></a><span data-ttu-id="4a3c6-103">Constantes Factoid</span><span class="sxs-lookup"><span data-stu-id="4a3c6-103">Factoid Constants</span></span>

<span data-ttu-id="4a3c6-104">Définit des valeurs de chaîne constantes qui sont utilisées pour augmenter la précision de la reconnaissance en fournissant des informations contextuelles au module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4a3c6-105">Nom</span><span class="sxs-lookup"><span data-stu-id="4a3c6-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4a3c6-106">Description</span><span class="sxs-lookup"><span data-stu-id="4a3c6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="4a3c6-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-108">Désactive tous les autres Factoids et dictionnaires.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="4a3c6-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-110">Le paramètre par défaut pour Factoids pour les langues occidentales comprend le dictionnaire système, le dictionnaire de l’utilisateur, les différents signes de ponctuation et le Web et le numéro Factoid.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="4a3c6-111">Le paramètre par défaut pour Factoids pour les langues d’Extrême-Orient comprend tous les caractères pris en charge par le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="4a3c6-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-113">Indique à un module de reconnaissance pour utiliser le dictionnaire système uniquement.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="4a3c6-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-115">Indique à un module de reconnaissance pour utiliser une liste de mots définie par programmation.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="4a3c6-116">La liste de mots est définie par la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>propriété liste</strong></a> de mots d’un objet <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4a3c6-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-117">Si une chaîne est ajoutée à une liste de mots, ses versions en majuscules sont également ajoutées de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="4a3c6-118">Par exemple, l’ajout de &quot; Hello &quot; ajoute implicitement Hello &quot; &quot; et &quot; Hello &quot; .</span><span class="sxs-lookup"><span data-stu-id="4a3c6-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="4a3c6-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-120">Indique à un module de reconnaissance pour rechercher une adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-121">Une adresse de messagerie complète, telle que &quot; someone@example.com &quot; , doit être utilisée pour ce Factoid.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="4a3c6-122">Un alias solitaire, tel qu’un &quot; individu &quot; , n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="4a3c6-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-124">Indique à un module de reconnaissance pour rechercher une adresse Web.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="4a3c6-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-126">Indique à un module de reconnaissance pour rechercher un caractère unique.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-127">Ce Factoid recherche tout caractère ANSI isolé.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="4a3c6-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-129">Indique à un module de reconnaissance pour rechercher un nombre.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-130">Les valeurs numériques incluent les séparateurs, les décimales, les ordinaux et d’autres symboles numériques couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="4a3c6-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-132">Indique à un module de reconnaissance pour rechercher un chiffre unique, de 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="4a3c6-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-134">Fournit un contexte numérique simple à un module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-135">Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="4a3c6-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-137">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="4a3c6-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-139">Indique à un module de reconnaissance pour rechercher les codes postaux.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="4a3c6-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-141">Indique à un module de reconnaissance pour rechercher les pourcentages.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="4a3c6-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-143">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une date.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="4a3c6-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-145">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une heure.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="4a3c6-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-147">Indique à un module de reconnaissance pour rechercher des caractères qui désignent un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="4a3c6-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-149">Indique à un module de reconnaissance pour rechercher des caractères qui désignent un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="4a3c6-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-151">Indique à un module de reconnaissance pour rechercher un caractère majuscule unique : de A à Z.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="4a3c6-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-153">Indique à un module de reconnaissance pour rechercher un seul caractère en minuscules : de A à Z.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-154">Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="4a3c6-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-156">Indique à un module de reconnaissance pour rechercher les caractères de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-157">Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="4a3c6-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-159">Indique à un module de reconnaissance pour rechercher des caractères Kanji, katakana et Hiragana couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="4a3c6-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-161">Indique à un module de reconnaissance pour rechercher les caractères chinois simplifié couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="4a3c6-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-163">Indique à un module de reconnaissance pour rechercher les caractères chinois traditionnel couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="4a3c6-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-165">Indique à un module de reconnaissance pour rechercher les caractères coréens couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="4a3c6-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-167">Indique à un module de reconnaissance pour rechercher des caractères Hiragana uniquement.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="4a3c6-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-169">Indique à un module de reconnaissance pour rechercher des caractères katakana uniquement.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="4a3c6-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-171">Indique à un module de reconnaissance pour rechercher des caractères Kanji couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="4a3c6-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-173">Indique à un module de reconnaissance pour rechercher les caractères Kanji rarement utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-174">Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="4a3c6-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-176">Indique à un module de reconnaissance pour rechercher des caractères Bopomofo.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="4a3c6-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-178">Indique à un module de reconnaissance pour rechercher les caractères Jamos de compatibilité hangûl.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="4a3c6-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-180">Indique à un module de reconnaissance pour rechercher des caractères Hangul couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="4a3c6-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4a3c6-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4a3c6-182">Indique à un module de reconnaissance pour rechercher les caractères Hangul rarement utilisés.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a3c6-183">Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="4a3c6-184">Notes</span><span class="sxs-lookup"><span data-stu-id="4a3c6-184">Remarks</span></span>

<span data-ttu-id="4a3c6-185">En C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, situé dans le <systemdrive> \\ répertoire : Program Files \\ Microsoft Tablet PC Platform SDK \\ include si vous avez installé le kit de développement logiciel (SDK) à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="4a3c6-186">Ces constantes sont WCHARs, et non BSTR.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="4a3c6-187">Elles doivent être converties en BSTR avant d’être utilisées comme paramètres pour les méthodes d’objet.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="4a3c6-188">Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="4a3c6-189">Pour les détecteurs de script latin, les Factoids définis dans cette classe sont fournis uniquement à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="4a3c6-190">Pour les nouveaux développements, il est recommandé d’utiliser les valeurs définies dans la fonction [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) .</span><span class="sxs-lookup"><span data-stu-id="4a3c6-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="4a3c6-191">Pour plus d’informations, consultez [utilisation du contexte pour améliorer la précision](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="4a3c6-192">Utilisez ces identificateurs pour spécifier les Factoid à utiliser lors de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="4a3c6-193">Les combinaisons de Factoids suivantes sont prises en charge uniquement pour les langues occidentales.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="4a3c6-194">Ils n’ont pas de définitions distinctes, mais sont des entrées de littéral de chaîne acceptables dans la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) d’objets qui utilisent Factoids.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="4a3c6-195">Ces constantes de chaîne Factoid permettent à l’entrée de correspondre à l’un des Factoids dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="4a3c6-196">Combinaison</span><span class="sxs-lookup"><span data-stu-id="4a3c6-196">Combination</span></span>               | <span data-ttu-id="4a3c6-197">Définition</span><span class="sxs-lookup"><span data-stu-id="4a3c6-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4a3c6-198">« la rubrique WEB \| »</span><span class="sxs-lookup"><span data-stu-id="4a3c6-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="4a3c6-199">Factoid Web ou liste de mots.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="4a3c6-200">« courrier électronique \| »</span><span class="sxs-lookup"><span data-stu-id="4a3c6-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="4a3c6-201">Factoid d’E-mail ou liste de mots.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="4a3c6-202">« NOM du fichier \| Web \| »</span><span class="sxs-lookup"><span data-stu-id="4a3c6-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="4a3c6-203">Nom de fichier Factoid ou Factoid Web ou liste de mots.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="4a3c6-204">Si vous utilisez le contrôle [InkEdit](inkedit-control-reference.md) , Factoid peut être défini en tant que propriété du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="4a3c6-205">Si vous utilisez les API de la plateforme Tablet PC, vous pouvez définir la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) sur un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="4a3c6-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="4a3c6-206">Vous pouvez également définir cette propriété avec la constante de chaîne Factoid réelle.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="4a3c6-207">Les constantes de chaîne Factoid sont sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="4a3c6-208">Pour plus d’informations sur les Factoids et leur utilisation, consultez Utilisation du contexte pour [améliorer la précision](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="4a3c6-209">Pour déterminer si un Factoid est disponible dans un langage spécifique, consultez [Factoids pris en charge à partir de la version 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="4a3c6-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a3c6-210">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a3c6-210">Requirements</span></span>



| <span data-ttu-id="4a3c6-211">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a3c6-211">Requirement</span></span> | <span data-ttu-id="4a3c6-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a3c6-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3c6-213">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a3c6-213">Minimum supported client</span></span><br/> | <span data-ttu-id="4a3c6-214">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a3c6-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4a3c6-215">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a3c6-215">Minimum supported server</span></span><br/> | <span data-ttu-id="4a3c6-216">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a3c6-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4a3c6-217">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a3c6-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a3c6-218"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3c6-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a3c6-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a3c6-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a3c6-220">[**Factoid, propriété \[ InkRecognizeContext, classe\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="4a3c6-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="4a3c6-221">[**Factoid, propriété \[ PenInputPanel, classe\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="4a3c6-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="4a3c6-222">[**Propriété Factoid \[ InkEdit, contrôle\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="4a3c6-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="4a3c6-223">Utilisation du contexte pour améliorer la précision</span><span class="sxs-lookup"><span data-stu-id="4a3c6-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="4a3c6-224">Factoids pris en charge à partir de la version 1</span><span class="sxs-lookup"><span data-stu-id="4a3c6-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

