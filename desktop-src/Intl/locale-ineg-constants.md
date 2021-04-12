---
description: Cette rubrique définit les \_ \* constantes INEG des paramètres régionaux utilisés par nls.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Constantes LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318573"
---
# <a name="locale_ineg-constants"></a><span data-ttu-id="8b999-103">Paramètres régionaux \_ INEG \* constantes</span><span class="sxs-lookup"><span data-stu-id="8b999-103">LOCALE\_INEG\* Constants</span></span>

<span data-ttu-id="8b999-104">Cette rubrique définit les \_ \* constantes INEG des paramètres régionaux utilisés par nls.</span><span class="sxs-lookup"><span data-stu-id="8b999-104">This topic defines the LOCALE\_INEG\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b999-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b999-105">Value</span></span></th>
<th><span data-ttu-id="8b999-106">Signification</span><span class="sxs-lookup"><span data-stu-id="8b999-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b999-107">LOCALE_INEGCURR</span><span class="sxs-lookup"><span data-stu-id="8b999-107">LOCALE_INEGCURR</span></span></td>
<td><span data-ttu-id="8b999-108">Mode de devise négative.</span><span class="sxs-lookup"><span data-stu-id="8b999-108">Negative currency mode.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8b999-109">Mode</span><span class="sxs-lookup"><span data-stu-id="8b999-109">Mode</span></span></th>
<th><span data-ttu-id="8b999-110">Format pour une devise négative</span><span class="sxs-lookup"><span data-stu-id="8b999-110">Format for negative currency</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b999-111">0</span><span class="sxs-lookup"><span data-stu-id="8b999-111">0</span></span></td>
<td><span data-ttu-id="8b999-112">Parenthèse ouvrante, symbole monétaire, nombre, parenthèse droite ; par exemple, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="8b999-112">Left parenthesis, monetary symbol, number, right parenthesis; for example, ($1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-113">1</span><span class="sxs-lookup"><span data-stu-id="8b999-113">1</span></span></td>
<td><span data-ttu-id="8b999-114">Signe négatif, symbole monétaire, nombre ; par exemple,-$1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-114">Negative sign, monetary symbol, number; for example, -$1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-115">2</span><span class="sxs-lookup"><span data-stu-id="8b999-115">2</span></span></td>
<td><span data-ttu-id="8b999-116">Symbole monétaire, signe négatif, nombre ; par exemple, $-1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-116">Monetary symbol, negative sign, number; for example, $-1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-117">3</span><span class="sxs-lookup"><span data-stu-id="8b999-117">3</span></span></td>
<td><span data-ttu-id="8b999-118">Symbole monétaire, nombre, signe négatif ; par exemple, $1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-118">Monetary symbol, number, negative sign; for example, $1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-119">4</span><span class="sxs-lookup"><span data-stu-id="8b999-119">4</span></span></td>
<td><span data-ttu-id="8b999-120">Parenthèse ouvrante, nombre, symbole monétaire, parenthèse droite ; par exemple, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="8b999-120">Left parenthesis, number, monetary symbol, right parenthesis; for example, (1.1$)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-121">5</span><span class="sxs-lookup"><span data-stu-id="8b999-121">5</span></span></td>
<td><span data-ttu-id="8b999-122">Signe négatif, nombre, symbole monétaire ; par exemple,-$1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-122">Negative sign, number, monetary symbol; for example, -1.1$</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-123">6</span><span class="sxs-lookup"><span data-stu-id="8b999-123">6</span></span></td>
<td><span data-ttu-id="8b999-124">Nombre, signe négatif, symbole monétaire ; par exemple, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="8b999-124">Number, negative sign, monetary symbol; for example, 1.1-$</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-125">7</span><span class="sxs-lookup"><span data-stu-id="8b999-125">7</span></span></td>
<td><span data-ttu-id="8b999-126">Nombre, symbole monétaire, signe négatif ; par exemple, $1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-126">Number, monetary symbol, negative sign; for example, 1.1$-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-127">8</span><span class="sxs-lookup"><span data-stu-id="8b999-127">8</span></span></td>
<td><span data-ttu-id="8b999-128">Signe négatif, nombre, espace, symbole monétaire (comme #5, mais avec un espace avant le symbole monétaire); par exemple,-$1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-128">Negative sign, number, space, monetary symbol (like #5, but with a space before the monetary symbol); for example, -1.1 $</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-129">9</span><span class="sxs-lookup"><span data-stu-id="8b999-129">9</span></span></td>
<td><span data-ttu-id="8b999-130">Le signe négatif, le symbole monétaire, l’espace, le nombre (comme #1, mais avec un espace après le symbole monétaire); par exemple,-$1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-130">Negative sign, monetary symbol, space, number (like #1, but with a space after the monetary symbol); for example, -$ 1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-131">10</span><span class="sxs-lookup"><span data-stu-id="8b999-131">10</span></span></td>
<td><span data-ttu-id="8b999-132">Nombre, espace, symbole monétaire, signe négatif (comme #7, mais avec un espace avant le symbole monétaire); par exemple, $1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-132">Number, space, monetary symbol, negative sign (like #7, but with a space before the monetary symbol); for example, 1.1 $-</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-133">11</span><span class="sxs-lookup"><span data-stu-id="8b999-133">11</span></span></td>
<td><span data-ttu-id="8b999-134">Symbole monétaire, espace, nombre, signe négatif (comme #3, mais avec un espace après le symbole monétaire); par exemple, $1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-134">Monetary symbol, space, number, negative sign (like #3, but with a space after the monetary symbol); for example, $ 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-135">12</span><span class="sxs-lookup"><span data-stu-id="8b999-135">12</span></span></td>
<td><span data-ttu-id="8b999-136">Symbole monétaire, espace, signe négatif, nombre (comme #2, mais avec un espace après le symbole monétaire); par exemple, $-1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-136">Monetary symbol, space, negative sign, number (like #2, but with a space after the monetary symbol); for example, $ -1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-137">13</span><span class="sxs-lookup"><span data-stu-id="8b999-137">13</span></span></td>
<td><span data-ttu-id="8b999-138">Nombre, signe négatif, espace, symbole monétaire (comme #6, mais avec un espace avant le symbole monétaire); par exemple, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="8b999-138">Number, negative sign, space, monetary symbol (like #6, but with a space before the monetary symbol); for example, 1.1- $</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-139">14</span><span class="sxs-lookup"><span data-stu-id="8b999-139">14</span></span></td>
<td><span data-ttu-id="8b999-140">Parenthèse ouvrante, symbole monétaire, espace, nombre, parenthèse droite (comme #0, mais avec un espace après le symbole monétaire); par exemple, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="8b999-140">Left parenthesis, monetary symbol, space, number, right parenthesis (like #0, but with a space after the monetary symbol); for example, ($ 1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-141">15</span><span class="sxs-lookup"><span data-stu-id="8b999-141">15</span></span></td>
<td><span data-ttu-id="8b999-142">Parenthèse ouvrante, nombre, espace, symbole monétaire, parenthèse droite (comme #4, mais avec un espace avant le symbole monétaire); par exemple, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="8b999-142">Left parenthesis, number, space, monetary symbol, right parenthesis (like #4, but with a space before the monetary symbol); for example, (1.1 $)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-143">LOCALE_INEGNUMBER</span><span class="sxs-lookup"><span data-stu-id="8b999-143">LOCALE_INEGNUMBER</span></span></td>
<td><span data-ttu-id="8b999-144">Mode de nombre négatif, autrement dit, le format d’un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="8b999-144">Negative number mode, that is, the format for a negative number.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8b999-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b999-145">Value</span></span></th>
<th><span data-ttu-id="8b999-146">Format</span><span class="sxs-lookup"><span data-stu-id="8b999-146">Format</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b999-147">0</span><span class="sxs-lookup"><span data-stu-id="8b999-147">0</span></span></td>
<td><span data-ttu-id="8b999-148">Parenthèse ouvrante, nombre, parenthèse droite ; par exemple, (1,1)</span><span class="sxs-lookup"><span data-stu-id="8b999-148">Left parenthesis, number, right parenthesis; for example, (1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-149">1</span><span class="sxs-lookup"><span data-stu-id="8b999-149">1</span></span></td>
<td><span data-ttu-id="8b999-150">Signe négatif, nombre ; par exemple,-1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-150">Negative sign, number; for example, -1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-151">2</span><span class="sxs-lookup"><span data-stu-id="8b999-151">2</span></span></td>
<td><span data-ttu-id="8b999-152">Signe négatif, espace, nombre ; par exemple,-1,1</span><span class="sxs-lookup"><span data-stu-id="8b999-152">Negative sign, space, number; for example, - 1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-153">3</span><span class="sxs-lookup"><span data-stu-id="8b999-153">3</span></span></td>
<td><span data-ttu-id="8b999-154">Nombre, signe négatif ; par exemple, 1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-154">Number, negative sign; for example, 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-155">4</span><span class="sxs-lookup"><span data-stu-id="8b999-155">4</span></span></td>
<td><span data-ttu-id="8b999-156">Nombre, espace, signe négatif ; par exemple, 1,1-</span><span class="sxs-lookup"><span data-stu-id="8b999-156">Number, space, negative sign; for example, 1.1 -</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-157">LOCALE_INEGSEPBYSPACE</span><span class="sxs-lookup"><span data-stu-id="8b999-157">LOCALE_INEGSEPBYSPACE</span></span></td>
<td><span data-ttu-id="8b999-158">Séparation du signe négatif dans une valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="8b999-158">Separation of the negative sign in a monetary value.</span></span> <span data-ttu-id="8b999-159">Cette valeur est 1 si le symbole monétaire est séparé par un espace de la quantité négative, ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b999-159">This value is 1 if the monetary symbol is separated by a space from the negative amount, or 0 if it is not.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-160">LOCALE_INEGSIGNPOSN</span><span class="sxs-lookup"><span data-stu-id="8b999-160">LOCALE_INEGSIGNPOSN</span></span></td>
<td><span data-ttu-id="8b999-161">Index de mise en forme pour les valeurs de devise de la connexion négative.</span><span class="sxs-lookup"><span data-stu-id="8b999-161">Formatting index for the negative sign in currency values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8b999-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b999-162">Value</span></span></th>
<th><span data-ttu-id="8b999-163">Signification</span><span class="sxs-lookup"><span data-stu-id="8b999-163">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b999-164">0</span><span class="sxs-lookup"><span data-stu-id="8b999-164">0</span></span></td>
<td><span data-ttu-id="8b999-165">Les parenthèses entourent le montant et le symbole monétaire.</span><span class="sxs-lookup"><span data-stu-id="8b999-165">Parentheses surround the amount and the monetary symbol.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-166">1</span><span class="sxs-lookup"><span data-stu-id="8b999-166">1</span></span></td>
<td><span data-ttu-id="8b999-167">Le signe précède le nombre.</span><span class="sxs-lookup"><span data-stu-id="8b999-167">The sign precedes the number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-168">2</span><span class="sxs-lookup"><span data-stu-id="8b999-168">2</span></span></td>
<td><span data-ttu-id="8b999-169">Le signe suit le nombre.</span><span class="sxs-lookup"><span data-stu-id="8b999-169">The sign follows the number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b999-170">3</span><span class="sxs-lookup"><span data-stu-id="8b999-170">3</span></span></td>
<td><span data-ttu-id="8b999-171">Le signe précède le symbole monétaire.</span><span class="sxs-lookup"><span data-stu-id="8b999-171">The sign precedes the monetary symbol.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-172">4</span><span class="sxs-lookup"><span data-stu-id="8b999-172">4</span></span></td>
<td><span data-ttu-id="8b999-173">Le signe suit le symbole monétaire.</span><span class="sxs-lookup"><span data-stu-id="8b999-173">The sign follows the monetary symbol.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b999-174">LOCALE_INEGSYMPRECEDES</span><span class="sxs-lookup"><span data-stu-id="8b999-174">LOCALE_INEGSYMPRECEDES</span></span></td>
<td><span data-ttu-id="8b999-175">Position du symbole monétaire dans une valeur monétaire négative.</span><span class="sxs-lookup"><span data-stu-id="8b999-175">Position of the monetary symbol in a negative monetary value.</span></span> <span data-ttu-id="8b999-176">Cette valeur est 1 si le symbole monétaire précède la quantité négative, ou 0 si le symbole suit la valeur.</span><span class="sxs-lookup"><span data-stu-id="8b999-176">This value is 1 if the monetary symbol precedes the negative amount, or 0 if the symbol follows the amount.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



