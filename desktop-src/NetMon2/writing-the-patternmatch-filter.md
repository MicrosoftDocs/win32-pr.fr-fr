---
description: Le filtre de correspondance de modèle indique au pilote d’accepter des frames ayant un modèle spécifique à un décalage spécifique.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Écriture du filtre PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542929"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="f0ec3-103">Écriture du filtre PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="f0ec3-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="f0ec3-104">Le filtre de correspondance de modèle indique au pilote d’accepter des frames ayant un modèle spécifique à un décalage spécifique.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="f0ec3-105">Vous pouvez spécifier au maximum quatre correspondances de modèle détaillées, qui peuvent être combinées dans des instructions AND logiques ou ou pour l’évaluation d’un pilote Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="f0ec3-106">Pour implémenter des correspondances de modèle, utilisez les structures de Moniteur réseau suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0ec3-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="f0ec3-107">**FORMULE**</span><span class="sxs-lookup"><span data-stu-id="f0ec3-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="f0ec3-108">**ANDEXP**</span><span class="sxs-lookup"><span data-stu-id="f0ec3-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="f0ec3-109">**PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="f0ec3-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="f0ec3-110">Pour évaluer une instruction **ou** , combinez deux à quatre modèles correspondant à une structure [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="f0ec3-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="f0ec3-111">Pour évaluer une instruction AND, associez-en une à quatre structures **ANDEXP** et une structure d' [**EXPRESSION**](expression.md) (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="f0ec3-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="f0ec3-112">Définitions de correspondance de modèle</span><span class="sxs-lookup"><span data-stu-id="f0ec3-112">Pattern Match Definitions</span></span>

<span data-ttu-id="f0ec3-113">Une correspondance de modèle unique est définie par la structure [**PATTERNMATCH**](patternmatch.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ec3-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="f0ec3-114">Une correspondance individuelle peut fonctionner de l’une des deux façons suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="f0ec3-115">Normalement, le pilote prend le décalage (qui peut être \_ basé sur le décalage \_ par rapport \_ au frame, à la base du \_ décalage \_ \_ par rapport \_ au \_ protocole effectif, à la \_ \_ base du décalage par rapport à \_ \_ \_ IPX ou à la base du décalage \_ par rapport à l' \_ \_ \_ adresse IP) et commence à compter à cet endroit.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="f0ec3-116">Le pilote compte le décalage d’octets à partir de là, puis correspond aux données qu’il trouve avec les octets de la première longueur dans **PatternToMatch**.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="f0ec3-117">S’ils sont identiques et si les indicateurs de \_ correspondance de modèle \_ \_ ne sont pas définis, alors ce modèle réussit.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="f0ec3-118">S’ils sont différents et que les \_ indicateurs de correspondance de modèle \_ \_ n’ont pas été définis, le modèle est réussi.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="f0ec3-119">Dans le cas contraire, ce modèle échoue.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="f0ec3-120">Ou :</span><span class="sxs-lookup"><span data-stu-id="f0ec3-120">Or:</span></span>

<span data-ttu-id="f0ec3-121">Si l' \_ indicateur de port indicateurs de correspondance de modèle \_ \_ \_ spécifié est défini et que la base est définie sur la base du décalage \_ \_ par rapport \_ au \_ protocole IPX ou à la base du décalage \_ \_ par rapport \_ à l' \_ adresse IP, la comparaison est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="f0ec3-122">Tout d’abord, le pilote s’assure que le protocole de base de décalage est présent, puis le pilote vérifie que le port spécifié correspond au port dans le frame.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="f0ec3-123">Enfin, le pilote s’assure que le membre **PatternToMatch** correspond à avant, à l’exception près que le décalage est à partir de la fin de l’adresse IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="f0ec3-124">Notez que si la base n’est pas l’une de ces deux, l' \_ indicateur de port indicateurs de correspondance de modèle \_ spécifié est \_ \_ ignoré et le modèle est évalué comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="f0ec3-125">Pour évaluer une correspondance de modèle unique, une structure d' [**expression**](expression.md) doit avoir un membre **AndExp** contenant une correspondance de modèle unique.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="f0ec3-126">La création du filtre de correspondance de modèle implique la création de structures [**PATTERNMATCH**](patternmatch.md) et leur combinaison logique avec les structures [**expression**](expression.md) et [**ANDEXP**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ec3-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="f0ec3-127">**Pour écrire un filtre PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="f0ec3-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="f0ec3-128">Dans la structure [**ANDEXP**](andexp.md) , remplissez le tableau avec des correspondances de modèle.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="f0ec3-129">Remplissez la structure de l' [**expression**](expression.md) avec un tableau de membres **AndExp** .</span><span class="sxs-lookup"><span data-stu-id="f0ec3-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="f0ec3-130">Ne dépassez pas un total de quatre correspondances de modèle pour le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="f0ec3-131">Dans la structure [**PATTERNMATCH**](patternmatch.md) , sélectionnez un type d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="f0ec3-132">Sélectionnez une base de décalage.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="f0ec3-133">Énumérer une valeur de port.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="f0ec3-134">Définissez la valeur de décalage.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-134">Define offset value.</span></span>
8.  <span data-ttu-id="f0ec3-135">Définissez la longueur du modèle.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="f0ec3-136">Énumérez la valeur du modèle.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="f0ec3-137">Exemples PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="f0ec3-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="f0ec3-138">Ce frame représente un décalage standard.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-138">This frame represents a standard offset.</span></span>

![frame de décalage standard](images/offs-pat.png)

<span data-ttu-id="f0ec3-140">Le fragment de code est implémenté comme suit :</span><span class="sxs-lookup"><span data-stu-id="f0ec3-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="f0ec3-141">Ce frame représente un décalage spécifié par le port (par rapport à IPX).</span><span class="sxs-lookup"><span data-stu-id="f0ec3-141">This frame depicts a port-specified offset (against IPX).</span></span>

![trame de décalage spécifiée par le port](images/stan-pat.png)

<span data-ttu-id="f0ec3-143">L’exemple de code est implémenté comme suit :</span><span class="sxs-lookup"><span data-stu-id="f0ec3-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



