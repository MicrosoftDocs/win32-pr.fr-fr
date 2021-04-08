---
description: Paramètres régionaux \_ SMONTHNAME \* constantes
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: Constantes LOCALE_SMONTHNAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752804"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="bd6a6-103">Paramètres régionaux \_ SMONTHNAME \* constantes</span><span class="sxs-lookup"><span data-stu-id="bd6a6-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="bd6a6-104">Cette rubrique définit les \_ \* constantes SMONTHNAME des paramètres régionaux utilisés par nls.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd6a6-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd6a6-105">Value</span></span></th>
<th><span data-ttu-id="bd6a6-106">Signification</span><span class="sxs-lookup"><span data-stu-id="bd6a6-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd6a6-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="bd6a6-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="bd6a6-108">Nom long natif de janvier.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-108">Native long name for January.</span></span> <span data-ttu-id="bd6a6-109">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bd6a6-110">L’appel de la fonction <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> avec une constante LOCALE_SMONTHNAME \* retourne la forme autonome ou de nom du mois.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="bd6a6-111">Pour obtenir la forme génitif du nom du mois, l’application appelle <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> ou <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> avec une image de date de ddMMMM et supprime les deux chiffres à partir du début de la chaîne récupérée.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="bd6a6-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="bd6a6-113">Nom long natif pour février.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-113">Native long name for February.</span></span> <span data-ttu-id="bd6a6-114">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-115">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="bd6a6-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="bd6a6-117">Nom long natif pour mars.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-117">Native long name for March.</span></span> <span data-ttu-id="bd6a6-118">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-119">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="bd6a6-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="bd6a6-121">Nom long natif pour avril.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-121">Native long name for April.</span></span> <span data-ttu-id="bd6a6-122">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-123">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="bd6a6-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="bd6a6-125">Nom long natif pour mai.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-125">Native long name for May.</span></span> <span data-ttu-id="bd6a6-126">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-127">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="bd6a6-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="bd6a6-129">Nom long natif pour juin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-129">Native long name for June.</span></span> <span data-ttu-id="bd6a6-130">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-131">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="bd6a6-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="bd6a6-133">Nom long natif pour juillet.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-133">Native long name for July.</span></span> <span data-ttu-id="bd6a6-134">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-135">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="bd6a6-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="bd6a6-137">Nom long natif pour août.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-137">Native long name for August.</span></span> <span data-ttu-id="bd6a6-138">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-139">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="bd6a6-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="bd6a6-141">Nom long natif pour septembre.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-141">Native long name for September.</span></span> <span data-ttu-id="bd6a6-142">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-143">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="bd6a6-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="bd6a6-145">Nom long natif pour octobre.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-145">Native long name for October.</span></span> <span data-ttu-id="bd6a6-146">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-147">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="bd6a6-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="bd6a6-149">Nom long natif pour novembre.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-149">Native long name for November.</span></span> <span data-ttu-id="bd6a6-150">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-151">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd6a6-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="bd6a6-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="bd6a6-153">Nom long natif pour décembre.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-153">Native long name for December.</span></span> <span data-ttu-id="bd6a6-154">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-155">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd6a6-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="bd6a6-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="bd6a6-157">Nom natif pour un 13e mois, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="bd6a6-158">Le nombre maximal de caractères autorisés pour cette chaîne est 80, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bd6a6-159">Consultez la remarque pour LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="bd6a6-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




