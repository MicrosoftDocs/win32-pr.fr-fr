---
description: La fonction DATEADD effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date. Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Fonction DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112434"
---
# <a name="dateadd-function"></a><span data-ttu-id="e97b3-104">Fonction DATEADD</span><span class="sxs-lookup"><span data-stu-id="e97b3-104">DATEADD Function</span></span>

<span data-ttu-id="e97b3-105">La fonction DATEADD effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date.</span><span class="sxs-lookup"><span data-stu-id="e97b3-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="e97b3-106">Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.</span><span class="sxs-lookup"><span data-stu-id="e97b3-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="e97b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e97b3-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="e97b3-108">Arguments</span><span class="sxs-lookup"><span data-stu-id="e97b3-108">Arguments</span></span>

<span data-ttu-id="e97b3-109">*DateTimeUnits*</span><span class="sxs-lookup"><span data-stu-id="e97b3-109">*DateTimeUnits*</span></span>

<span data-ttu-id="e97b3-110">Spécifie les unités du paramètre *DateTime* : année, trimestre, mois, semaine, jour, heure, minute ou seconde.</span><span class="sxs-lookup"><span data-stu-id="e97b3-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="e97b3-111">Cette valeur respecte la casse et les guillemets ne sont pas requis autour du paramètre.</span><span class="sxs-lookup"><span data-stu-id="e97b3-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="e97b3-112">*OffsetValue*</span><span class="sxs-lookup"><span data-stu-id="e97b3-112">*OffsetValue*</span></span>

<span data-ttu-id="e97b3-113">Spécifie l’offset de temps, dans les unités spécifiées par le paramètre *DateTimeUnits* .</span><span class="sxs-lookup"><span data-stu-id="e97b3-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="e97b3-114">**OffsetValue** doit être un entier négatif.</span><span class="sxs-lookup"><span data-stu-id="e97b3-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="e97b3-115">Les valeurs positives ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e97b3-115">Positive values are not supported.</span></span>

<span data-ttu-id="e97b3-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e97b3-116">*DateTime*</span></span>

<span data-ttu-id="e97b3-117">Spécifie un horodatage à partir duquel calculer le décalage.</span><span class="sxs-lookup"><span data-stu-id="e97b3-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="e97b3-118">Il ne peut pas s’agir d’un littéral de date.</span><span class="sxs-lookup"><span data-stu-id="e97b3-118">This cannot be a date literal.</span></span> <span data-ttu-id="e97b3-119">Il doit s’agir de GETGMTDATE ou du résultat d’une autre fonction DATEADD.</span><span class="sxs-lookup"><span data-stu-id="e97b3-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="e97b3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e97b3-120">Remarks</span></span>

<span data-ttu-id="e97b3-121">La fonction DATEADD ne peut être utilisée que dans les comparaisons de valeurs littérales et uniquement à droite de l’opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="e97b3-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="e97b3-122">La fonction GETGMTDATE retourne la date et l’heure actuelles en heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="e97b3-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="e97b3-123">N’oubliez pas que cette valeur peut ne pas être la même que l’heure locale de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e97b3-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="e97b3-124">N’utilisez pas l’opérateur de comparaison égal à (=), car la représentation temporelle interne peut produire des erreurs d’arrondi qui aboutissent à des résultats de correspondance inattendus.</span><span class="sxs-lookup"><span data-stu-id="e97b3-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="e97b3-125">Vous pouvez utiliser plusieurs fonctions DATEADD pour combiner des unités de décalage.</span><span class="sxs-lookup"><span data-stu-id="e97b3-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="e97b3-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="e97b3-126">Examples</span></span>

<span data-ttu-id="e97b3-127">L’exemple suivant de clause WHERE correspond à des documents qui ont été modifiés au cours des cinq derniers jours :</span><span class="sxs-lookup"><span data-stu-id="e97b3-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="e97b3-128">L’exemple suivant de clause WHERE correspond à des documents qui ont été modifiés au cours des deux derniers jours et quatre heures :</span><span class="sxs-lookup"><span data-stu-id="e97b3-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="e97b3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e97b3-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e97b3-130">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="e97b3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e97b3-131">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="e97b3-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="e97b3-132">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="e97b3-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="e97b3-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e97b3-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e97b3-134">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="e97b3-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="e97b3-135">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="e97b3-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



