---
title: Chaînes
description: Cette section décrit les fonctions de chaîne.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- ressources, chaînes
- chaînes
- fonctions de chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732100"
---
# <a name="strings"></a><span data-ttu-id="29482-106">Chaînes</span><span class="sxs-lookup"><span data-stu-id="29482-106">Strings</span></span>

<span data-ttu-id="29482-107">Cette section décrit les fonctions de chaîne et explique comment les utiliser dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="29482-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="29482-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="29482-108">In This Section</span></span>



| <span data-ttu-id="29482-109">Nom</span><span class="sxs-lookup"><span data-stu-id="29482-109">Name</span></span>                                     | <span data-ttu-id="29482-110">Description</span><span class="sxs-lookup"><span data-stu-id="29482-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="29482-111">À propos des chaînes</span><span class="sxs-lookup"><span data-stu-id="29482-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="29482-112">Décrit les fonctions de chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="29482-113">À propos de strsafe. h</span><span class="sxs-lookup"><span data-stu-id="29482-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="29482-114">Décrit les fonctions de chaîne dans strsafe. h.</span><span class="sxs-lookup"><span data-stu-id="29482-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="29482-115">Référence de chaîne</span><span class="sxs-lookup"><span data-stu-id="29482-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="29482-116">Contient la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="29482-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="29482-117">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="29482-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29482-118">Nom</span><span class="sxs-lookup"><span data-stu-id="29482-118">Name</span></span></th>
<th><span data-ttu-id="29482-119">Description</span><span class="sxs-lookup"><span data-stu-id="29482-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29482-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="29482-121">Convertit une chaîne de caractères ou un caractère unique en minuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="29482-122">Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="29482-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="29482-124">Convertit les caractères majuscules d’une mémoire tampon en caractères minuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="29482-125">La fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="29482-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="29482-127">Récupère un pointeur vers le caractère suivant dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="29482-128">Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="29482-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="29482-130">Récupère le pointeur vers le caractère suivant dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="29482-131">Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="29482-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="29482-133">Récupère un pointeur vers le caractère précédent dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="29482-134">Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="29482-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="29482-136">Récupère le pointeur désignant le caractère précédent dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="29482-137">Cette fonction peut gérer des chaînes composées de caractères à une ou plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="29482-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="29482-139">Convertit une chaîne en jeu de caractères défini par l’OEM.</span><span class="sxs-lookup"><span data-stu-id="29482-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="29482-141">Convertit un nombre spécifié de caractères dans une chaîne en jeu de caractères défini par l’OEM.</span><span class="sxs-lookup"><span data-stu-id="29482-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="29482-143">Convertit une chaîne de caractères ou un seul caractère en majuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="29482-144">Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="29482-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="29482-146">Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="29482-147">La fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="29482-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="29482-149">Compare deux chaînes de caractères, à l’aide des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="29482-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="29482-150">Pour la compatibilité avec Unicode, utilisez <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> ou la version Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="29482-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="29482-152">Compare deux chaînes Unicode (caractères larges) à l’aide des paramètres régionaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="29482-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString devant</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="29482-154">Mappe une chaîne à une autre, en effectuant une option de transformation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="29482-156">Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="29482-157">Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie.</span><span class="sxs-lookup"><span data-stu-id="29482-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="29482-158">Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux.</span><span class="sxs-lookup"><span data-stu-id="29482-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="29482-160">Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="29482-161">Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie.</span><span class="sxs-lookup"><span data-stu-id="29482-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="29482-162">Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux.</span><span class="sxs-lookup"><span data-stu-id="29482-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="29482-163">Contrairement à ses parents proches <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> et <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> présente un comportement standard grâce à l’utilisation du commutateur <strong> # Unicode define</strong> .</span><span class="sxs-lookup"><span data-stu-id="29482-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="29482-164">Il s’agit de la fonction recommandée.</span><span class="sxs-lookup"><span data-stu-id="29482-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="29482-166">Récupère des informations de type caractère pour les caractères de la chaîne source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="29482-167">Pour chaque caractère de la chaîne, la fonction définit un ou plusieurs bits dans l’élément 16 bits correspondant du tableau de sortie.</span><span class="sxs-lookup"><span data-stu-id="29482-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="29482-168">Chaque bit identifie un type de caractère donné, par exemple si le caractère est une lettre, un chiffre ou aucun des deux.</span><span class="sxs-lookup"><span data-stu-id="29482-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="29482-170">Détermine si un caractère est un caractère alphabétique.</span><span class="sxs-lookup"><span data-stu-id="29482-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="29482-171">Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="29482-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="29482-173">Détermine si un caractère est un caractère alphabétique ou numérique.</span><span class="sxs-lookup"><span data-stu-id="29482-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="29482-174">Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="29482-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="29482-176">Détermine si un caractère est en minuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="29482-177">Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="29482-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="29482-179">Détermine si un caractère est en majuscules.</span><span class="sxs-lookup"><span data-stu-id="29482-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="29482-180">Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="29482-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="29482-182">Charge une ressource de chaîne à partir du fichier exécutable associé à un module spécifié, copie la chaîne dans une mémoire tampon et ajoute un caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="29482-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="29482-184">Ajoute une chaîne à une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="29482-186">Compare deux chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="29482-186">Compares two character strings.</span></span> <span data-ttu-id="29482-187">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="29482-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="29482-189">Compare deux chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="29482-189">Compares two character strings.</span></span> <span data-ttu-id="29482-190">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="29482-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="29482-192">Copie une chaîne dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="29482-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="29482-194">Copie un nombre spécifié de caractères d’une chaîne source dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="29482-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="29482-196">Détermine la longueur de la chaîne spécifiée (à l’exclusion du caractère null de fin).</span><span class="sxs-lookup"><span data-stu-id="29482-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="29482-198">Convertit une chaîne du jeu de caractères défini par l’OEM en une chaîne ANSI ou à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="29482-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="29482-200">Convertit un nombre spécifié de caractères dans une chaîne du jeu de caractères défini par l’OEM en une chaîne de caractères ANSI ou larges.</span><span class="sxs-lookup"><span data-stu-id="29482-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29482-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="29482-202">Écrit des données mises en forme dans la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29482-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="29482-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="29482-204">Écrit des données mises en forme dans la mémoire tampon spécifiée à l’aide d’un pointeur vers une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="29482-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="29482-205">Fonctions strsafe</span><span class="sxs-lookup"><span data-stu-id="29482-205">Strsafe Functions</span></span>



| <span data-ttu-id="29482-206">Nom</span><span class="sxs-lookup"><span data-stu-id="29482-206">Name</span></span>                                             | <span data-ttu-id="29482-207">Description</span><span class="sxs-lookup"><span data-stu-id="29482-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29482-208">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="29482-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="29482-209">Concatène une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="29482-210">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="29482-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="29482-211">Concatène une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="29482-212">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="29482-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="29482-213">Concatène le nombre spécifié d’octets d’une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="29482-214">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="29482-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="29482-215">Concatène le nombre spécifié d’octets d’une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="29482-216">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="29482-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="29482-217">Copie une chaîne dans une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="29482-218">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="29482-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="29482-219">Copie une chaîne dans une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="29482-220">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="29482-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="29482-221">Copie le nombre d’octets spécifié d’une chaîne vers une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="29482-222">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="29482-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="29482-223">Copie le nombre d’octets spécifié d’une chaîne vers une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="29482-224">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="29482-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="29482-225">Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="29482-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="29482-226">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="29482-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="29482-227">Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="29482-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="29482-228">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="29482-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="29482-229">Détermine si une chaîne dépasse la longueur spécifiée, en octets.</span><span class="sxs-lookup"><span data-stu-id="29482-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="29482-230">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="29482-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="29482-231">Écrit des données mises en forme dans la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="29482-232">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="29482-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="29482-233">Écrit des données mises en forme dans la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="29482-234">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="29482-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="29482-235">Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="29482-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="29482-236">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="29482-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="29482-237">Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="29482-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="29482-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="29482-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="29482-239">Concatène une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="29482-240">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="29482-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="29482-241">Concatène une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="29482-242">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="29482-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="29482-243">Concatène le nombre spécifié de caractères d’une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="29482-244">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="29482-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="29482-245">Concatène le nombre spécifié de caractères d’une chaîne à une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="29482-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="29482-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="29482-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="29482-247">Copie une chaîne dans une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="29482-248">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="29482-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="29482-249">Copie une chaîne dans une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="29482-250">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="29482-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="29482-251">Copie le nombre spécifié de caractères d’une chaîne vers une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="29482-252">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="29482-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="29482-253">Copie le nombre spécifié de caractères d’une chaîne vers une autre.</span><span class="sxs-lookup"><span data-stu-id="29482-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="29482-254">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="29482-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="29482-255">Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="29482-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="29482-256">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="29482-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="29482-257">Obtient une ligne de texte à partir de stdin, jusqu’à et y compris le caractère de saut de ligne (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="29482-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="29482-258">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="29482-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="29482-259">Détermine si une chaîne dépasse la longueur spécifiée, en caractères.</span><span class="sxs-lookup"><span data-stu-id="29482-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="29482-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="29482-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="29482-261">Écrit des données mises en forme dans la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="29482-262">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="29482-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="29482-263">Écrit des données mises en forme dans la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29482-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="29482-264">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="29482-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="29482-265">Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="29482-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="29482-266">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="29482-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="29482-267">Écrit des données mises en forme dans la chaîne spécifiée à l’aide d’un pointeur vers une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="29482-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

