---
description: ICE65 vérifie que la table d’environnement ne possède pas de valeurs de préfixe ou d’ajout non valides.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545070"
---
# <a name="ice65"></a><span data-ttu-id="a5bd5-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="a5bd5-103">ICE65</span></span>

<span data-ttu-id="a5bd5-104">ICE65 vérifie que la [table d’environnement](environment-table.md) ne possède pas de valeurs de préfixe ou d’ajout non valides.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="a5bd5-105">L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICE65 provoque généralement des problèmes d’installation, de désinstallation ou de réparation de la variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="a5bd5-106">Par exemple, seules certaines valeurs d’une variable particulière peuvent être supprimées si une ou plusieurs des valeurs de cette variable ont un séparateur de fin.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="a5bd5-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="a5bd5-107">Result</span></span>

<span data-ttu-id="a5bd5-108">ICE65 publie un avertissement ou une erreur si la table d’environnement contient des valeurs de préfixe ou d’ajout non valides.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="a5bd5-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5bd5-109">Example</span></span>

<span data-ttu-id="a5bd5-110">ICE65 signale l’erreur et l’avertissement suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="a5bd5-111">La valeur null de fin à la fin de la valeur ( \[ ~ \] ) marque cette valeur comme étant ajoutée à toute valeur existante.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="a5bd5-112">Le caractère situé juste avant la valeur null (point-virgule) devient le séparateur de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="a5bd5-113">Cette valeur comporte également un point-virgule au début de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="a5bd5-114">Pour corriger cette erreur, supprimez simplement le point-virgule de début.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="a5bd5-115">La valeur null de début dans la valeur ( \[ ~ \] ) marque cette valeur à ajouter à toute valeur existante.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="a5bd5-116">Le caractère situé juste après la valeur null devient le séparateur de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="a5bd5-117">Dans ce cas, ce caractère est la lettre « e », qui se produit également au milieu de la chaîne à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="a5bd5-118">Cette condition (avec un séparateur identique à un caractère dans la chaîne à ajouter) peut provoquer des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="a5bd5-119">La lettre « e », en tant que lettre courante, est susceptible d’être trouvée dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="a5bd5-120">Un meilleur choix serait « ; » ou un autre caractère non alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="a5bd5-121">(Toutefois, si la valeur est un chemin d’accès, «  : » et « \\ » et «» sont des choix risqués.)</span><span class="sxs-lookup"><span data-stu-id="a5bd5-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="a5bd5-122">Pour résoudre cet avertissement, utilisez un autre caractère de séparation.</span><span class="sxs-lookup"><span data-stu-id="a5bd5-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="a5bd5-123">Table d’environnement</span><span class="sxs-lookup"><span data-stu-id="a5bd5-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="a5bd5-124">Composant</span><span class="sxs-lookup"><span data-stu-id="a5bd5-124">Component</span></span> | <span data-ttu-id="a5bd5-125">Répertoire</span><span class="sxs-lookup"><span data-stu-id="a5bd5-125">Directory</span></span> | <span data-ttu-id="a5bd5-126">Attributs</span><span class="sxs-lookup"><span data-stu-id="a5bd5-126">Attributes</span></span>         | <span data-ttu-id="a5bd5-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="a5bd5-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="a5bd5-128">Var1</span><span class="sxs-lookup"><span data-stu-id="a5bd5-128">Var1</span></span>      | <span data-ttu-id="a5bd5-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="a5bd5-129">TestVar</span></span>   | <span data-ttu-id="a5bd5-130">\[~\]; AppendThis</span><span class="sxs-lookup"><span data-stu-id="a5bd5-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="a5bd5-131">TestComponent</span><span class="sxs-lookup"><span data-stu-id="a5bd5-131">TestComponent</span></span> |
| <span data-ttu-id="a5bd5-132">Var2</span><span class="sxs-lookup"><span data-stu-id="a5bd5-132">Var2</span></span>      | <span data-ttu-id="a5bd5-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="a5bd5-133">TestVar</span></span>   | <span data-ttu-id="a5bd5-134">\[~\]eAppendThis</span><span class="sxs-lookup"><span data-stu-id="a5bd5-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="a5bd5-135">TestComponent</span><span class="sxs-lookup"><span data-stu-id="a5bd5-135">TestComponent</span></span> |
| <span data-ttu-id="a5bd5-136">Var3</span><span class="sxs-lookup"><span data-stu-id="a5bd5-136">Var3</span></span>      | <span data-ttu-id="a5bd5-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="a5bd5-137">TestVar</span></span>   | <span data-ttu-id="a5bd5-138">; PrependThis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="a5bd5-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="a5bd5-139">TestComponent</span><span class="sxs-lookup"><span data-stu-id="a5bd5-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a5bd5-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5bd5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5bd5-141">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="a5bd5-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



