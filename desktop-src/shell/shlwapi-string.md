---
description: Cette section décrit les fonctions de gestion des chaînes de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion des chaînes de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952832"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="12692-104">Fonctions de gestion des chaînes de Shell</span><span class="sxs-lookup"><span data-stu-id="12692-104">Shell String Handling Functions</span></span>

<span data-ttu-id="12692-105">Cette section décrit les fonctions de gestion des chaînes de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="12692-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="12692-106">Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="12692-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12692-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="12692-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12692-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="12692-108">Topic</span></span></th>
<th><span data-ttu-id="12692-109">Description</span><span class="sxs-lookup"><span data-stu-id="12692-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12692-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-111">Effectue une comparaison entre deux caractères.</span><span class="sxs-lookup"><span data-stu-id="12692-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="12692-112">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-114">Récupère une chaîne utilisée avec des sites Web lors de la spécification des préférences linguistiques.</span><span class="sxs-lookup"><span data-stu-id="12692-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-116">Effectue une comparaison respectant la casse d’un nombre spécifié de caractères à partir du début de deux chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="12692-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-118">Effectue une comparaison ne respectant pas la casse d’un nombre spécifié de caractères à partir du début de deux chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="12692-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-120">Compare un nombre spécifié de caractères à partir du début de deux chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="12692-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-122">Détermine si un caractère représente un espace.</span><span class="sxs-lookup"><span data-stu-id="12692-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-124">Extrait une ressource de texte spécifiée lorsque cette ressource est fournie sous la forme d’une chaîne indirecte (une chaîne commençant par le symbole' @ ').</span><span class="sxs-lookup"><span data-stu-id="12692-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-126">Effectue une copie d’une chaîne dans la mémoire nouvellement allouée.</span><span class="sxs-lookup"><span data-stu-id="12692-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-128">Ajoute une chaîne à une autre.</span><span class="sxs-lookup"><span data-stu-id="12692-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-129">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="12692-129">Do not use.</span></span> <span data-ttu-id="12692-130">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-132">Copie et ajoute des caractères d’une chaîne à la fin d’une autre.</span><span class="sxs-lookup"><span data-stu-id="12692-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-133">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="12692-133">Do not use.</span></span> <span data-ttu-id="12692-134">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-136">Concatène deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="12692-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="12692-137">Utilisé lorsque des concaténations répétées dans la même mémoire tampon sont requises.</span><span class="sxs-lookup"><span data-stu-id="12692-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-139">Recherche dans une chaîne la première occurrence d’un caractère qui correspond au caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="12692-140">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-142">Recherche dans une chaîne la première occurrence d’un caractère qui correspond au caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="12692-143">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-145">Recherche dans une chaîne la première occurrence d’un caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="12692-146">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-148">Recherche dans une chaîne la première occurrence d’un caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="12692-149">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-151">Compare deux chaînes pour déterminer si elles sont identiques.</span><span class="sxs-lookup"><span data-stu-id="12692-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="12692-152">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-154">Compare les chaînes à l’aide des règles de classement du runtime C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="12692-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="12692-155">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-157">Compare deux chaînes pour déterminer si elles sont identiques.</span><span class="sxs-lookup"><span data-stu-id="12692-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="12692-158">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-160">Compare deux chaînes à l’aide de règles de classement Runtime C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="12692-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="12692-161">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-163">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="12692-163">Compares two Unicode strings.</span></span> <span data-ttu-id="12692-164">Les chiffres dans les chaînes sont considérés comme du contenu numérique plutôt que du texte.</span><span class="sxs-lookup"><span data-stu-id="12692-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="12692-165">Ce test ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-167">Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer s’ils sont identiques.</span><span class="sxs-lookup"><span data-stu-id="12692-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="12692-168">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="12692-169">La macro <strong>StrNCmp</strong> diffère de cette fonction dans nom uniquement.</span><span class="sxs-lookup"><span data-stu-id="12692-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-171">Compare un nombre spécifié de caractères à partir du début de deux chaînes à l’aide des règles de classement Runtime C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="12692-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="12692-172">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-174">Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer s’ils sont identiques.</span><span class="sxs-lookup"><span data-stu-id="12692-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="12692-175">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="12692-176">La macro <strong>StrNCmpI</strong> diffère de cette fonction dans nom uniquement.</span><span class="sxs-lookup"><span data-stu-id="12692-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-178">Compare un nombre spécifié de caractères à partir du début de deux chaînes à l’aide des règles de classement Runtime C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="12692-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="12692-179">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-181">Copie une chaîne dans une autre.</span><span class="sxs-lookup"><span data-stu-id="12692-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-182">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="12692-182">Do not use.</span></span> <span data-ttu-id="12692-183">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-185">Copie un nombre spécifié de caractères à partir du début d’une chaîne vers une autre.</span><span class="sxs-lookup"><span data-stu-id="12692-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-186">N’utilisez pas cette fonction ou la macro <strong>StrNCpy</strong> .</span><span class="sxs-lookup"><span data-stu-id="12692-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="12692-187">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-189">Recherche dans une chaîne la première occurrence d’un groupe de caractères.</span><span class="sxs-lookup"><span data-stu-id="12692-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="12692-190">La méthode de recherche respecte la casse et le caractère <strong>null</strong> de fin est inclus dans la correspondance du modèle de recherche.</span><span class="sxs-lookup"><span data-stu-id="12692-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-192">Recherche dans une chaîne la première occurrence d’un groupe de caractères.</span><span class="sxs-lookup"><span data-stu-id="12692-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="12692-193">La méthode de recherche ne respecte pas la casse et le caractère <strong>null</strong> de fin est inclus dans la correspondance du modèle de recherche.</span><span class="sxs-lookup"><span data-stu-id="12692-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-195">Duplique une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-197">Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille.</span><span class="sxs-lookup"><span data-stu-id="12692-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-199">Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille.</span><span class="sxs-lookup"><span data-stu-id="12692-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="12692-200">Diffère de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> dans un type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="12692-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-202">Convertit une valeur numérique en une chaîne qui représente le nombre en octets, en kilo-octets, en mégaoctets ou en gigaoctets, selon la taille.</span><span class="sxs-lookup"><span data-stu-id="12692-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="12692-203">Étend <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> en offrant la possibilité d’arrondir au chiffre le plus proche affiché ou de supprimer les chiffres incomplets.</span><span class="sxs-lookup"><span data-stu-id="12692-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-205">Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille.</span><span class="sxs-lookup"><span data-stu-id="12692-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="12692-206">Diffère de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> dans un type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="12692-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-208">Convertit une valeur numérique en une chaîne qui représente le nombre exprimé en kilo-octets comme valeur de taille.</span><span class="sxs-lookup"><span data-stu-id="12692-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-210">Convertit un intervalle de temps, exprimé en millisecondes, en une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-212">Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer si elles sont égales.</span><span class="sxs-lookup"><span data-stu-id="12692-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-214">Ajoute un nombre spécifié de caractères à partir du début d’une chaîne à la fin d’un autre.</span><span class="sxs-lookup"><span data-stu-id="12692-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-215">N’utilisez pas cette fonction ou la macro <strong>StrCatN</strong> .</span><span class="sxs-lookup"><span data-stu-id="12692-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="12692-216">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-218">Recherche dans une chaîne la première occurrence d’un caractère contenu dans une mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="12692-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="12692-219">Cette recherche n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="12692-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-221">Recherche dans une chaîne la dernière occurrence d’un caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="12692-222">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-224">Recherche dans une chaîne la dernière occurrence d’un caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="12692-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="12692-225">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-227">Accepte une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> qui contient ou pointe vers une chaîne, et retourne cette chaîne en tant que <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12692-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-229">Convertit une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> en une chaîne, puis place le résultat dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="12692-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-231">Prend une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> et retourne un pointeur vers une chaîne allouée contenant le nom complet.</span><span class="sxs-lookup"><span data-stu-id="12692-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-233">Prend une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a>, le convertit en une chaîne et place le résultat dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="12692-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-235">Recherche la dernière occurrence d’une sous-chaîne spécifiée dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="12692-236">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-238">Obtient la longueur d’une sous-chaîne dans une chaîne composée uniquement de caractères contenus dans une mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="12692-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-240">Recherche la première occurrence d’une sous-chaîne dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="12692-241">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-243">Recherche la première occurrence d’une sous-chaîne dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="12692-244">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="12692-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-246">Convertit une chaîne qui représente une valeur décimale en entier.</span><span class="sxs-lookup"><span data-stu-id="12692-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="12692-247">La macro <strong>StrToLong</strong> est identique à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="12692-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-249">Convertit une chaîne représentant une valeur décimale ou hexadécimale en entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="12692-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-251">Convertit une chaîne représentant un nombre décimal ou hexadécimal en entier.</span><span class="sxs-lookup"><span data-stu-id="12692-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-253">Supprime les caractères de début et de fin spécifiés d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="12692-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12692-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-255">Prend une liste d’arguments de longueur variable et retourne les valeurs des arguments sous la forme d’une chaîne mise en forme de style <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12692-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-256">N’utilisez pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="12692-256">Do not use this function.</span></span> <span data-ttu-id="12692-257">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12692-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="12692-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="12692-259">Prend une liste d’arguments et retourne les valeurs des arguments sous la forme d’une chaîne mise en forme de style <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="12692-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="12692-260">N’utilisez pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="12692-260">Do not use this function.</span></span> <span data-ttu-id="12692-261">Pour connaître les autres fonctions, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="12692-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
