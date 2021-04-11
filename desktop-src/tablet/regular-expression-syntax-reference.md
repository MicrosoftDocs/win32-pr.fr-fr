---
description: Vous pouvez définir et assigner des étendues d’entrée personnalisées à l’aide de la syntaxe d’expression régulière d’écriture qui est comprise par certains des reconnaissance de l’écriture manuscrite Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Référence de syntaxe des expressions régulières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211181"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="f24fd-103">Référence de syntaxe des expressions régulières</span><span class="sxs-lookup"><span data-stu-id="f24fd-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="f24fd-104">Vous pouvez définir et assigner des étendues d’entrée personnalisées à l’aide de la syntaxe d’expression régulière d’écriture qui est comprise par certains des reconnaissance de l’écriture manuscrite Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f24fd-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="f24fd-105">La syntaxe est un sous-ensemble de l' [implémentation du langage des expressions régulières](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f24fd-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="f24fd-106">Il existe des différences dans la façon dont les expressions régulières d’écriture manuscrite sont utilisées et la façon dont les autres types d’expressions régulières sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="f24fd-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="f24fd-107">La syntaxe d’écriture manuscrite est utilisée pour spécifier une chaîne exacte qui sera mise en correspondance par le moteur de reconnaissance et non une sous-chaîne.</span><span class="sxs-lookup"><span data-stu-id="f24fd-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="f24fd-108">Par exemple, l’expression régulière s ( \[ a-z \] +) p retourne des correspondances pour « soupe », « stop », « InStep » et « esophagus ».</span><span class="sxs-lookup"><span data-stu-id="f24fd-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="f24fd-109">En revanche, une expression régulière d’écriture équivalente telle que s ( ! est \_ ONECHAR) + p correspondrait à « soupe » et à « Stop », mais pas à « InStep » et à « esophagus ».</span><span class="sxs-lookup"><span data-stu-id="f24fd-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="f24fd-110">Les expressions régulières d’écriture manuscrite ne prennent pas en charge les espaces insécables dans les expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="f24fd-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="f24fd-111">Autrement dit, vous ne pouvez pas utiliser l’entité « nbsp » dans une expression régulière d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="f24fd-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="f24fd-112">Les sections suivantes décrivent plus en détail la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="f24fd-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="f24fd-113">Opérateurs valides</span><span class="sxs-lookup"><span data-stu-id="f24fd-113">Valid Operators</span></span>

<span data-ttu-id="f24fd-114">Les opérateurs suivants sont valides pour la création d’expressions régulières afin de définir des étendues d’entrée pour les reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="f24fd-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="f24fd-115">Opérateur</span><span class="sxs-lookup"><span data-stu-id="f24fd-115">Operator</span></span>      | <span data-ttu-id="f24fd-116">Description</span><span class="sxs-lookup"><span data-stu-id="f24fd-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="f24fd-117">Opérateur unaire postfix signifiant zéro, une ou plusieurs occurrences de l’opérande.</span><span class="sxs-lookup"><span data-stu-id="f24fd-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="f24fd-118">Postfix opérateur unaire signifiant une ou plusieurs occurrences de l’opérande.</span><span class="sxs-lookup"><span data-stu-id="f24fd-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="f24fd-119">?</span><span class="sxs-lookup"><span data-stu-id="f24fd-119">?</span></span><br/>  | <span data-ttu-id="f24fd-120">Opérateur unaire postfix signifiant zéro ou une occurrence de l’opérande.</span><span class="sxs-lookup"><span data-stu-id="f24fd-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="f24fd-121">Signification de l’opérateur d’infixe binaire « or ».</span><span class="sxs-lookup"><span data-stu-id="f24fd-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="f24fd-122">()</span><span class="sxs-lookup"><span data-stu-id="f24fd-122">()</span></span><br/> | <span data-ttu-id="f24fd-123">Utilisé pour regrouper des éléments.</span><span class="sxs-lookup"><span data-stu-id="f24fd-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="f24fd-124">L’implémentation Microsoft d’expressions régulières pour les reconnaissance de l’écriture manuscrite permet d’obtenir des applications répétées d’opérateurs unaires suffixés.</span><span class="sxs-lookup"><span data-stu-id="f24fd-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="f24fd-125">Par exemple, a \* \* = (a \* ) \* = a \* , b ??</span><span class="sxs-lookup"><span data-stu-id="f24fd-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="f24fd-126">= (b ?) ?</span><span class="sxs-lookup"><span data-stu-id="f24fd-126">= (b?)?</span></span> <span data-ttu-id="f24fd-127">= b ?.</span><span class="sxs-lookup"><span data-stu-id="f24fd-127">= b?.</span></span> <span data-ttu-id="f24fd-128">Elles autorisent également les répétitions non consécutives, par exemple : a \* ? \* = ((a \* ) ?) \* = (a \* ) \* = a \* .</span><span class="sxs-lookup"><span data-stu-id="f24fd-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="f24fd-129">Cela diffère de .NET Framework expressions régulières, qui n’autorisent que le ?</span><span class="sxs-lookup"><span data-stu-id="f24fd-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="f24fd-130">opérateur à répéter.</span><span class="sxs-lookup"><span data-stu-id="f24fd-130">operator to be repeated.</span></span>

<span data-ttu-id="f24fd-131">Une autre différence par rapport à .NET Framework expressions régulières est que les expressions régulières d’écriture ne prennent pas en charge une expression vide désignée avec une paire de parenthèses vide ().</span><span class="sxs-lookup"><span data-stu-id="f24fd-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="f24fd-132">Seuls les caractères de la page de codes 1252 sont pris en charge pour les expressions régulières d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="f24fd-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="f24fd-133">Utilisation des étendues d’entrée</span><span class="sxs-lookup"><span data-stu-id="f24fd-133">Using Input Scopes</span></span>

<span data-ttu-id="f24fd-134">Vous pouvez également utiliser l’ensemble d’étendues d’entrée habituelles qui sont définies dans le cadre de la fonction [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) dans vos expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="f24fd-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="f24fd-135">Par exemple, la valeur du mois (numérique) est \_ date \_ mois.</span><span class="sxs-lookup"><span data-stu-id="f24fd-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="f24fd-136">La syntaxe permettant de spécifier une étendue d’entrée dans le cadre d’une expression régulière consiste à ajouter la valeur énumérée de l’étendue d’entrée à une parenthèse ouvrante et à un point d’exclamation ( !, et à placer une parenthèse fermante,) à la fin.</span><span class="sxs-lookup"><span data-stu-id="f24fd-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="f24fd-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f24fd-137">For example:</span></span>

<span data-ttu-id="f24fd-138">( ! Est \_ mois de la DATE \_ )</span><span class="sxs-lookup"><span data-stu-id="f24fd-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="f24fd-139">Si vous combinez l' \_ étendue d’entrée par défaut en Oring avec toute autre étendue d’entrée, l’effet est que le module de reconnaissance peut retourner une expression unique prise en charge par le modèle de langage par défaut (par exemple, un mot du dictionnaire système ou une date) avec ou sans ponctuation, ou toute valeur qui remplit le reste de l’expression régulière transmise au module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="f24fd-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="f24fd-140">Les membres suivants de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) ne sont pas pris en charge dans les expressions régulières : est \_ PHRASELIST, IS \_ REGULAREXPRESSION, is \_ SRGS, is \_ XML.</span><span class="sxs-lookup"><span data-stu-id="f24fd-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="f24fd-141">Opérateurs non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f24fd-141">Unsupported Operators</span></span>

<span data-ttu-id="f24fd-142">Les opérateurs d’expression régulière suivants ne sont pas pris en charge lors de la création d’expressions régulières d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="f24fd-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="f24fd-143">Opérateur</span><span class="sxs-lookup"><span data-stu-id="f24fd-143">Operator</span></span>                                     | <span data-ttu-id="f24fd-144">Description</span><span class="sxs-lookup"><span data-stu-id="f24fd-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f24fd-145">.</span><span class="sxs-lookup"><span data-stu-id="f24fd-145">.</span></span><br/>                                 | <span data-ttu-id="f24fd-146">Caractère point.</span><span class="sxs-lookup"><span data-stu-id="f24fd-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="f24fd-147">Crochets.</span><span class="sxs-lookup"><span data-stu-id="f24fd-147">Square brackets.</span></span> <span data-ttu-id="f24fd-148">Utilisez des parenthèses pour regrouper des éléments.</span><span class="sxs-lookup"><span data-stu-id="f24fd-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="f24fd-149">Accolades.</span><span class="sxs-lookup"><span data-stu-id="f24fd-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="f24fd-150">(?\# Commentaire) et un \# \[ Commentaire\]</span><span class="sxs-lookup"><span data-stu-id="f24fd-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="f24fd-151">Comments :</span><span class="sxs-lookup"><span data-stu-id="f24fd-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="f24fd-152">Caractère de signe dollar.</span><span class="sxs-lookup"><span data-stu-id="f24fd-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="f24fd-153">Caractère de signe insertion.</span><span class="sxs-lookup"><span data-stu-id="f24fd-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="f24fd-154">Caractère tiret.</span><span class="sxs-lookup"><span data-stu-id="f24fd-154">Dash character.</span></span> <span data-ttu-id="f24fd-155">Doit ou ( \| ) rassembler tous les ensembles d’éléments.</span><span class="sxs-lookup"><span data-stu-id="f24fd-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="f24fd-156">Caractères d'échappement</span><span class="sxs-lookup"><span data-stu-id="f24fd-156">Escaping Characters</span></span>

<span data-ttu-id="f24fd-157">Les caractères ordinaires, autres que ceux figurant dans le tableau suivant, correspondent à eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="f24fd-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="f24fd-158">Autrement dit, un « a » dans une expression régulière spécifie que l’entrée doit correspondre à un « a ».</span><span class="sxs-lookup"><span data-stu-id="f24fd-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="f24fd-159">Une autre différence importante dans l’écriture d’expressions régulières d’écriture manuscrite est que vous pouvez uniquement échapper un ensemble limité de caractères dans une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="f24fd-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="f24fd-160">Le tableau suivant présente le jeu de caractères autorisé qui peut être placé dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="f24fd-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="f24fd-161">Toute autre tentative d’échappement d’un caractère entraînera la levée d’une erreur par le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="f24fd-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="f24fd-162">Caractère</span><span class="sxs-lookup"><span data-stu-id="f24fd-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="f24fd-163">\\?</span><span class="sxs-lookup"><span data-stu-id="f24fd-163">\\?</span></span><br/>  |
| <span data-ttu-id="f24fd-164">\\(</span><span class="sxs-lookup"><span data-stu-id="f24fd-164">\\(</span></span><br/>  |
| <span data-ttu-id="f24fd-165">\\)</span><span class="sxs-lookup"><span data-stu-id="f24fd-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="f24fd-166">\\!</span><span class="sxs-lookup"><span data-stu-id="f24fd-166">\\!</span></span><br/>  |
| <span data-ttu-id="f24fd-167">\\.</span><span class="sxs-lookup"><span data-stu-id="f24fd-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="f24fd-168">\\{</span><span class="sxs-lookup"><span data-stu-id="f24fd-168">\\{</span></span><br/>  |
| <span data-ttu-id="f24fd-169">\\}</span><span class="sxs-lookup"><span data-stu-id="f24fd-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 