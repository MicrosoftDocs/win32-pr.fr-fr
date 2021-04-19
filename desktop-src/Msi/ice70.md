---
description: ICE70 vérifie que les valeurs entières pour les entrées de Registre sont spécifiées correctement.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520660"
---
# <a name="ice70"></a><span data-ttu-id="0ac21-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="0ac21-103">ICE70</span></span>

<span data-ttu-id="0ac21-104">ICE70 vérifie que les valeurs entières pour les entrées de Registre sont spécifiées correctement.</span><span class="sxs-lookup"><span data-stu-id="0ac21-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="0ac21-105">Les valeurs de la forme \# \# Str, \# % non développé Str ne sont pas validées.</span><span class="sxs-lookup"><span data-stu-id="0ac21-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="0ac21-106">Les valeurs de la forme \# xhex, \# xhex, \# Integer et \# \[ Property \] sont validées.</span><span class="sxs-lookup"><span data-stu-id="0ac21-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="0ac21-107">Le tableau suivant fournit une brève vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="0ac21-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="0ac21-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ac21-108">Value</span></span>                 | <span data-ttu-id="0ac21-109">Validation</span><span class="sxs-lookup"><span data-stu-id="0ac21-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0ac21-110">\#\#Str</span><span class="sxs-lookup"><span data-stu-id="0ac21-110">\#\#str</span></span>               | <span data-ttu-id="0ac21-111">valide</span><span class="sxs-lookup"><span data-stu-id="0ac21-111">valid</span></span>                                                                         |
| <span data-ttu-id="0ac21-112">\#% non développé</span><span class="sxs-lookup"><span data-stu-id="0ac21-112">\#%unexpanded str</span></span>     | <span data-ttu-id="0ac21-113">valide</span><span class="sxs-lookup"><span data-stu-id="0ac21-113">valid</span></span>                                                                         |
| <span data-ttu-id="0ac21-114">\#xHex, \# xHex</span><span class="sxs-lookup"><span data-stu-id="0ac21-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="0ac21-115">Validez les caractères hexadécimaux valides (0-9, a-f, A-F).</span><span class="sxs-lookup"><span data-stu-id="0ac21-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="0ac21-116">Les propriétés sont autorisées ici.</span><span class="sxs-lookup"><span data-stu-id="0ac21-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="0ac21-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="0ac21-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="0ac21-118">Validez les caractères numériques valides (0-9).</span><span class="sxs-lookup"><span data-stu-id="0ac21-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="0ac21-119">Les propriétés sont autorisées ici.</span><span class="sxs-lookup"><span data-stu-id="0ac21-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="0ac21-120">La syntaxe d’une valeur entière à entrer dans le Registre est un \# entier où entier est numérique.</span><span class="sxs-lookup"><span data-stu-id="0ac21-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="0ac21-121">Résultats</span><span class="sxs-lookup"><span data-stu-id="0ac21-121">Result</span></span>

<span data-ttu-id="0ac21-122">ICE70 signale une erreur si les valeurs entières pour les entrées de registre ne sont pas spécifiées correctement.</span><span class="sxs-lookup"><span data-stu-id="0ac21-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="0ac21-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ac21-123">Example</span></span>

<span data-ttu-id="0ac21-124">ICE70 signale les erreurs suivantes pour l’exemple donné.</span><span class="sxs-lookup"><span data-stu-id="0ac21-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="0ac21-125">Pour corriger cette erreur : Si vous souhaitez que la valeur soit numérique, modifiez la valeur pour utiliser tous les caractères numériques.</span><span class="sxs-lookup"><span data-stu-id="0ac21-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="0ac21-126">Si vous souhaitez que la valeur soit une chaîne, elle doit être précédée de deux' \# ' ( \# \# ) au lieu d’un seul.</span><span class="sxs-lookup"><span data-stu-id="0ac21-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="0ac21-127">Pour corriger cette erreur : les caractères hexadécimaux valides sont 0-9, A-F et a-f.</span><span class="sxs-lookup"><span data-stu-id="0ac21-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="0ac21-128">Seuls ces caractères peuvent être suivis de \# x (ou \# x).</span><span class="sxs-lookup"><span data-stu-id="0ac21-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="0ac21-129">[Table du Registre](registry-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0ac21-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="0ac21-130">Registre</span><span class="sxs-lookup"><span data-stu-id="0ac21-130">Registry</span></span> | <span data-ttu-id="0ac21-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ac21-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="0ac21-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="0ac21-132">Reg1</span></span>     | <span data-ttu-id="0ac21-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="0ac21-133">\#12xz34</span></span> |
| <span data-ttu-id="0ac21-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="0ac21-134">Reg2</span></span>     | <span data-ttu-id="0ac21-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="0ac21-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="0ac21-136">Notes</span><span class="sxs-lookup"><span data-stu-id="0ac21-136">Remarks</span></span>

-   <span data-ttu-id="0ac21-137">\#\[MyProperty \] est valide.</span><span class="sxs-lookup"><span data-stu-id="0ac21-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="0ac21-138">\#\[MyProperty n’est pas valide (crochet de fin manquant).</span><span class="sxs-lookup"><span data-stu-id="0ac21-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="0ac21-139">\#\[myprop1 \] \[ myprop2 est valide.</span><span class="sxs-lookup"><span data-stu-id="0ac21-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="0ac21-140">(Même si la dernière parenthèse fermante ne contient pas le crochet de fin, myprop1 peut avoir la valeur \# Str, ce qui signifie que \# \# Str \[ myprop2, qui est valide</span><span class="sxs-lookup"><span data-stu-id="0ac21-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="0ac21-141">\#\]MyProperty \[ n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="0ac21-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="0ac21-142">Toute propriété incorporée dans une chaîne de valeur ne peut pas être dans le \[ \] formulaire $compkey, \[ \# filekey \] ou \[ ! filekey, \] car ces propriétés ne sont pas numériques.</span><span class="sxs-lookup"><span data-stu-id="0ac21-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="0ac21-143">Toutefois, il existe une exception, \# \[ MyProperty \] \[ $compkey \] (ou \[ \# filekey \] ou \[ ! filekey \] ) est valide, car, comme avec le précédent, \[ MyProperty \] peut évaluer en \# Str.</span><span class="sxs-lookup"><span data-stu-id="0ac21-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ac21-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ac21-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ac21-145">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="0ac21-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



