---
description: Décrit les formats de date pris en charge pour une utilisation dans la clause WHERE WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formats de date de WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865653"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="45298-103">Formats de date de WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="45298-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="45298-104">Outre le format **DateTime** WMI, les formats de date suivants sont pris en charge pour une utilisation dans **la clause WQL** WQL.</span><span class="sxs-lookup"><span data-stu-id="45298-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="45298-105">Le format d’heure affiché diffère selon les différents paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="45298-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="45298-106">Les scripts qui se connectent à des ordinateurs distants doivent spécifier l’heure au format approprié pour les paramètres régionaux de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="45298-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="45298-107">Par exemple, le États-Unis format de date et d’heure est MM-jj-aaaa.</span><span class="sxs-lookup"><span data-stu-id="45298-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="45298-108">Si un script sur un ordinateur américain se connecte à un ordinateur cible dont le format est JJ-MM-AAAA, les requêtes sont traitées sur l’ordinateur cible sous la forme JJ-MM-AAAA.</span><span class="sxs-lookup"><span data-stu-id="45298-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="45298-109">Pour éviter des résultats différents entre les paramètres régionaux, utilisez le format [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="45298-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="45298-110">Pour plus d’informations, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="45298-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="45298-111">Format</span><span class="sxs-lookup"><span data-stu-id="45298-111">Format</span></span></th>
<th><span data-ttu-id="45298-112">Description</span><span class="sxs-lookup"><span data-stu-id="45298-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45298-113">Mois [th] JJ [,] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="45298-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="45298-114">Mois (en lettres ou abrégées en trois lettres), jour, virgule facultative et année sur deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="45298-115">21 janvier 1932</span><span class="sxs-lookup"><span data-stu-id="45298-115">January 21, 1932</span></span><br />
<span data-ttu-id="45298-116">21 janvier 32</span><span class="sxs-lookup"><span data-stu-id="45298-116">January 21, 32</span></span><br />
<span data-ttu-id="45298-117">21 1932 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-117">Jan 21 1932</span></span><br />
<span data-ttu-id="45298-118">21 32 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-119">Mois [th] [,] aaaa</span><span class="sxs-lookup"><span data-stu-id="45298-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="45298-120">Mois (à l’aide de l’orthographe ou de l’abréviation de trois lettres), de la virgule facultative et de l’année à quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="45298-121">1932 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-121">January 1932</span></span><br />
<span data-ttu-id="45298-122">1932 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-123">Mois [th] [AA] aa jj</span><span class="sxs-lookup"><span data-stu-id="45298-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="45298-124">Mois (en lettres ou abrégées en trois lettres), année à deux ou quatre chiffres et jour.</span><span class="sxs-lookup"><span data-stu-id="45298-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="45298-125">1932 21 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-125">January 1932 21</span></span><br />
<span data-ttu-id="45298-126">32 21 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-127">JJ mois [th] [,] [] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="45298-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="45298-128">Jour du mois, mois (à l’aide d’un caractère épelé ou abrégé en trois lettres), virgule facultative, espace facultatif et année sur deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="45298-129">21 janvier, 1932</span><span class="sxs-lookup"><span data-stu-id="45298-129">21 January, 1932</span></span><br />
<span data-ttu-id="45298-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="45298-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-131">JJ [AA] YY mois [th]</span><span class="sxs-lookup"><span data-stu-id="45298-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="45298-132">Jour du mois, année sur deux ou quatre chiffres et mois (à l’aide d’un caractère épelé ou abrégé en trois lettres).</span><span class="sxs-lookup"><span data-stu-id="45298-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="45298-133">21 1932 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-134">[YY] YY mois [th] JJ</span><span class="sxs-lookup"><span data-stu-id="45298-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="45298-135">Année sur deux ou quatre chiffres, mois (à l’aide d’une orthographe ou d’une abréviation en trois lettres) et jour.</span><span class="sxs-lookup"><span data-stu-id="45298-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="45298-136">1932 janvier 21</span><span class="sxs-lookup"><span data-stu-id="45298-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-137">aaaa mois [th]</span><span class="sxs-lookup"><span data-stu-id="45298-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="45298-138">Année et mois sur deux ou quatre chiffres (à l’aide d’un caractère épelé ou abrégé en trois lettres).</span><span class="sxs-lookup"><span data-stu-id="45298-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="45298-139">1932 Jan</span><span class="sxs-lookup"><span data-stu-id="45298-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-140">AAAA JJ mois [th]</span><span class="sxs-lookup"><span data-stu-id="45298-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="45298-141">Année, jour et mois à deux ou quatre chiffres (à l’aide d’un caractère épelé ou abrégé en trois lettres).</span><span class="sxs-lookup"><span data-stu-id="45298-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="45298-142">1932 21 janvier</span><span class="sxs-lookup"><span data-stu-id="45298-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-143">Lecteur M {/-.} JJ {/-.} [AA] AA</span><span class="sxs-lookup"><span data-stu-id="45298-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="45298-144">Mois, jour et année sur deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="45298-145">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-146">JJ {/-.} Lecteur M {/-.} [AA] AA</span><span class="sxs-lookup"><span data-stu-id="45298-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="45298-147">Jour du mois, du mois et de l’année sur deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="45298-148">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-149">Lecteur M {/-.} [YY] yy {/-.} JJ</span><span class="sxs-lookup"><span data-stu-id="45298-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="45298-150">Mois, année à deux ou quatre chiffres, et jour.</span><span class="sxs-lookup"><span data-stu-id="45298-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="45298-151">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-152">JJ {/-.} [YY] yy {/-.} Lecteur Lecteur</span><span class="sxs-lookup"><span data-stu-id="45298-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="45298-153">Jour du mois, année sur deux ou quatre chiffres et mois.</span><span class="sxs-lookup"><span data-stu-id="45298-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="45298-154">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-155">[YY] yy {/-.} JJ {/-.} Lecteur Lecteur</span><span class="sxs-lookup"><span data-stu-id="45298-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="45298-156">Année, jour et mois à deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="45298-157">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-158">[YY] yy {/-.} Lecteur M {/-.} JJ</span><span class="sxs-lookup"><span data-stu-id="45298-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="45298-159">Année, mois et jour deux ou quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="45298-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="45298-160">Notez que les séparateurs doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="45298-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45298-161">[YY] AAMMJJ</span><span class="sxs-lookup"><span data-stu-id="45298-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="45298-162">Année, mois et jour deux ou quatre chiffres, sans espaces.</span><span class="sxs-lookup"><span data-stu-id="45298-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45298-163">YYYY [MM [JJ]]</span><span class="sxs-lookup"><span data-stu-id="45298-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="45298-164">Année à deux ou quatre chiffres, mois facultatif et jour facultatif, sans espaces.</span><span class="sxs-lookup"><span data-stu-id="45298-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="45298-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45298-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45298-166">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="45298-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




