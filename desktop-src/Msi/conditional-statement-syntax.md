---
description: Cette section décrit la syntaxe des instructions conditionnelles utilisées par la fonction MsiEvaluateCondition et les tables de séquences d’actions. Pour plus d’informations, consultez Exemples de syntaxe d’instruction conditionnelle.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Syntaxe d’instruction conditionnelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864409"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="200c6-104">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="200c6-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="200c6-105">Cette section décrit la syntaxe des instructions conditionnelles utilisées par la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) et les [tables de séquences](using-a-sequence-table.md)d’actions.</span><span class="sxs-lookup"><span data-stu-id="200c6-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="200c6-106">Pour plus d’informations, consultez [exemples de syntaxe d’instruction conditionnelle](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="200c6-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="200c6-107">Résumé de la syntaxe des instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="200c6-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="200c6-108">Ce tableau et la liste suivante résument la syntaxe à utiliser dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="200c6-109">Élément</span><span class="sxs-lookup"><span data-stu-id="200c6-109">Item</span></span>                | <span data-ttu-id="200c6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="200c6-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200c6-111">value</span><span class="sxs-lookup"><span data-stu-id="200c6-111">value</span></span>               | <span data-ttu-id="200c6-112">\|entier littéral de symbole \|</span><span class="sxs-lookup"><span data-stu-id="200c6-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="200c6-113">opérateur de comparaison</span><span class="sxs-lookup"><span data-stu-id="200c6-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="200c6-114">terme</span><span class="sxs-lookup"><span data-stu-id="200c6-114">term</span></span>                | <span data-ttu-id="200c6-115">\|Comparaison de valeurs de valeur-valeur d’opérateur \| (expression)\|</span><span class="sxs-lookup"><span data-stu-id="200c6-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="200c6-116">Facteur booléen</span><span class="sxs-lookup"><span data-stu-id="200c6-116">Boolean-factor</span></span>      | <span data-ttu-id="200c6-117">terme \| **non** terme</span><span class="sxs-lookup"><span data-stu-id="200c6-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="200c6-118">Terme booléen</span><span class="sxs-lookup"><span data-stu-id="200c6-118">Boolean-term</span></span>        | <span data-ttu-id="200c6-119">Facteur booléen de facteur booléen \| **et** terme</span><span class="sxs-lookup"><span data-stu-id="200c6-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="200c6-120">expression</span><span class="sxs-lookup"><span data-stu-id="200c6-120">expression</span></span>          | <span data-ttu-id="200c6-121">\|Expression **ou** expression booléenne à terme booléen</span><span class="sxs-lookup"><span data-stu-id="200c6-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="200c6-122">symbole</span><span class="sxs-lookup"><span data-stu-id="200c6-122">symbol</span></span>              | <span data-ttu-id="200c6-123">propriété \| % environment-variable \| $Component-action \| ? composant-State \| &Feature-action \| ! Feature-State</span><span class="sxs-lookup"><span data-stu-id="200c6-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="200c6-124">Les noms et les valeurs de symboles respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="200c6-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="200c6-125">Les noms des variables d’environnement ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="200c6-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="200c6-126">Le texte littéral doit être placé entre guillemets ("texte").</span><span class="sxs-lookup"><span data-stu-id="200c6-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="200c6-127">Le texte littéral qui contient des guillemets ne peut pas être utilisé dans des instructions conditionnelles, car il n’y a pas de caractère d’échappement pour les guillemets au sein du texte littéral.</span><span class="sxs-lookup"><span data-stu-id="200c6-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="200c6-128">Pour effectuer une comparaison avec un texte littéral contenant des guillemets, le texte littéral doit être placé dans une propriété.</span><span class="sxs-lookup"><span data-stu-id="200c6-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="200c6-129">Par exemple, pour vérifier que la propriété SERVERNAME ne contient pas de guillemets, définissez une propriété nommée QUOTes dans la [table Property](property-table.md) avec la valeur «et remplacez la condition par ServerName><quotes.</span><span class="sxs-lookup"><span data-stu-id="200c6-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="200c6-130">Les valeurs de propriété inexistantes sont traitées comme des chaînes vides.</span><span class="sxs-lookup"><span data-stu-id="200c6-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="200c6-131">Les valeurs numériques à virgule flottante ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="200c6-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="200c6-132">Les opérateurs et la priorité sont les mêmes que dans les langages de base et SQL.</span><span class="sxs-lookup"><span data-stu-id="200c6-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="200c6-133">Les opérateurs arithmétiques ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="200c6-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="200c6-134">Les parenthèses peuvent être utilisées pour substituer la priorité des opérateurs.</span><span class="sxs-lookup"><span data-stu-id="200c6-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="200c6-135">Les opérateurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="200c6-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="200c6-136">Pour les comparaisons de chaînes, un tilde « ~ » préfixé à l’opérateur effectue une comparaison qui ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="200c6-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="200c6-137">La comparaison d’un entier avec une valeur de chaîne ou de propriété qui ne peut pas être convertie en entier est toujours **msiEvaluateConditionFalse**, à l’exception de l’opérateur de comparaison « <> », qui retourne **msiEvaluateConditionTrue**.</span><span class="sxs-lookup"><span data-stu-id="200c6-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="200c6-138">Préfixes d’accès</span><span class="sxs-lookup"><span data-stu-id="200c6-138">Access Prefixes</span></span>

<span data-ttu-id="200c6-139">Le tableau suivant présente les préfixes à utiliser pour accéder aux différentes informations du système et du programme d’installation à utiliser dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="200c6-140">Type de symbole</span><span class="sxs-lookup"><span data-stu-id="200c6-140">Symbol type</span></span>          | <span data-ttu-id="200c6-141">Préfixe</span><span class="sxs-lookup"><span data-stu-id="200c6-141">Prefix</span></span> | <span data-ttu-id="200c6-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="200c6-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="200c6-143">Installer (propriété)</span><span class="sxs-lookup"><span data-stu-id="200c6-143">Installer property</span></span>   | <span data-ttu-id="200c6-144">(aucun)</span><span class="sxs-lookup"><span data-stu-id="200c6-144">(none)</span></span> | <span data-ttu-id="200c6-145">Valeur de la table de propriétés ([propriété](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="200c6-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="200c6-146">Variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="200c6-146">Environment variable</span></span> | %      | <span data-ttu-id="200c6-147">Valeur de la variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="200c6-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="200c6-148">Clé de la table des composants</span><span class="sxs-lookup"><span data-stu-id="200c6-148">Component table key</span></span>  | $      | <span data-ttu-id="200c6-149">État d’action du composant.</span><span class="sxs-lookup"><span data-stu-id="200c6-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="200c6-150">Clé de la table des composants</span><span class="sxs-lookup"><span data-stu-id="200c6-150">Component table key</span></span>  | <span data-ttu-id="200c6-151">?</span><span class="sxs-lookup"><span data-stu-id="200c6-151">?</span></span>      | <span data-ttu-id="200c6-152">État installé du composant.</span><span class="sxs-lookup"><span data-stu-id="200c6-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="200c6-153">Clé de la table de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="200c6-153">Feature table key</span></span>    | &      | <span data-ttu-id="200c6-154">État d’action de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="200c6-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="200c6-155">Clé de la table de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="200c6-155">Feature table key</span></span>    | <span data-ttu-id="200c6-156">!</span><span class="sxs-lookup"><span data-stu-id="200c6-156">!</span></span>      | <span data-ttu-id="200c6-157">État installé de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="200c6-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="200c6-158">Opérateurs logiques</span><span class="sxs-lookup"><span data-stu-id="200c6-158">Logical Operators</span></span>

<span data-ttu-id="200c6-159">Le tableau suivant montre les opérateurs logiques dans les expressions conditionnelles, dans l’ordre de priorité de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="200c6-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="200c6-160">Opérateur</span><span class="sxs-lookup"><span data-stu-id="200c6-160">Operator</span></span> | <span data-ttu-id="200c6-161">Signification</span><span class="sxs-lookup"><span data-stu-id="200c6-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="200c6-162">Not</span><span class="sxs-lookup"><span data-stu-id="200c6-162">Not</span></span>      | <span data-ttu-id="200c6-163">Prefix, opérateur unaire ; inverse l’état du terme suivant.</span><span class="sxs-lookup"><span data-stu-id="200c6-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="200c6-164">And</span><span class="sxs-lookup"><span data-stu-id="200c6-164">And</span></span>      | <span data-ttu-id="200c6-165">TRUE si les deux termes sont vrais.</span><span class="sxs-lookup"><span data-stu-id="200c6-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="200c6-166">ou</span><span class="sxs-lookup"><span data-stu-id="200c6-166">Or</span></span>       | <span data-ttu-id="200c6-167">TRUE si l’un des termes ou les deux sont vrais.</span><span class="sxs-lookup"><span data-stu-id="200c6-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="200c6-168">Xor</span><span class="sxs-lookup"><span data-stu-id="200c6-168">Xor</span></span>      | <span data-ttu-id="200c6-169">TRUE si les deux termes, mais pas les deux, ont la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="200c6-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="200c6-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="200c6-170">Eqv</span></span>      | <span data-ttu-id="200c6-171">TRUE si les deux termes sont TRUE ou si les deux termes ont la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="200c6-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="200c6-172">IMP</span><span class="sxs-lookup"><span data-stu-id="200c6-172">Imp</span></span>      | <span data-ttu-id="200c6-173">TRUE si le terme de gauche a la valeur FALSe ou si le terme à droite a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="200c6-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="200c6-174">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="200c6-174">Comparative Operators</span></span>

<span data-ttu-id="200c6-175">Le tableau suivant présente les opérateurs de comparaison utilisés dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="200c6-176">Ces opérateurs de comparaison peuvent uniquement se produire entre deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="200c6-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="200c6-177">Opérateur</span><span class="sxs-lookup"><span data-stu-id="200c6-177">Operator</span></span> | <span data-ttu-id="200c6-178">Signification</span><span class="sxs-lookup"><span data-stu-id="200c6-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="200c6-179">TRUE si la valeur de gauche est égale à la valeur de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="200c6-180">TRUE si la valeur de gauche n’est pas égale à la valeur de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="200c6-181">TRUE si la valeur de gauche est supérieure à la valeur de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="200c6-182">TRUE si la valeur de gauche est supérieure ou égale à la valeur droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="200c6-183">TRUE si la valeur de gauche est inférieure à la valeur de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="200c6-184">TRUE si la valeur de gauche est inférieure ou égale à la valeur droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="200c6-185">Opérateurs de sous-chaîne</span><span class="sxs-lookup"><span data-stu-id="200c6-185">Substring Operators</span></span>

<span data-ttu-id="200c6-186">Le tableau suivant montre les opérateurs de sous-chaîne utilisés dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="200c6-187">Les opérateurs de sous-chaîne peuvent se produire entre deux valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="200c6-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="200c6-188">Opérateur</span><span class="sxs-lookup"><span data-stu-id="200c6-188">Operator</span></span> | <span data-ttu-id="200c6-189">Signification</span><span class="sxs-lookup"><span data-stu-id="200c6-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="200c6-190">TRUE si la chaîne de gauche contient la chaîne de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="200c6-191">TRUE si la chaîne de gauche commence par la chaîne de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="200c6-192">TRUE si la chaîne de gauche se termine par la chaîne de droite.</span><span class="sxs-lookup"><span data-stu-id="200c6-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="200c6-193">Opérateurs numériques au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="200c6-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="200c6-194">Le tableau suivant montre les opérateurs numériques au niveau du bit dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="200c6-195">Ces opérateurs peuvent se produire entre deux valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="200c6-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="200c6-196">Opérateur</span><span class="sxs-lookup"><span data-stu-id="200c6-196">Operator</span></span> | <span data-ttu-id="200c6-197">Signification</span><span class="sxs-lookup"><span data-stu-id="200c6-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="200c6-198">And au niveau du bit, TRUE si les entiers de gauche et de droite ont des bits en commun.</span><span class="sxs-lookup"><span data-stu-id="200c6-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="200c6-199">True si les 16 bits de poids fort de l’entier gauche sont égaux à l’entier droit.</span><span class="sxs-lookup"><span data-stu-id="200c6-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="200c6-200">True si les 16 bits de poids faible de l’entier gauche sont égaux à l’entier droit.</span><span class="sxs-lookup"><span data-stu-id="200c6-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="200c6-201">Valeurs d’état des fonctionnalités et des composants</span><span class="sxs-lookup"><span data-stu-id="200c6-201">Feature and Component State Values</span></span>

<span data-ttu-id="200c6-202">Le tableau suivant indique où il est possible d’utiliser les symboles d’opérateur de composant et de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="200c6-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="200c6-203">And <state></span><span class="sxs-lookup"><span data-stu-id="200c6-203">Operator <state></span></span> | <span data-ttu-id="200c6-204">Où cette syntaxe est valide</span><span class="sxs-lookup"><span data-stu-id="200c6-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200c6-205">action $component</span><span class="sxs-lookup"><span data-stu-id="200c6-205">$component-action</span></span>      | <span data-ttu-id="200c6-206">Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="200c6-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="200c6-207">&fonctionnalité-action</span><span class="sxs-lookup"><span data-stu-id="200c6-207">&feature-action</span></span>        | <span data-ttu-id="200c6-208">Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="200c6-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="200c6-209">! fonctionnalité-État</span><span class="sxs-lookup"><span data-stu-id="200c6-209">!feature-state</span></span>         | <span data-ttu-id="200c6-210">Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="200c6-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="200c6-211">? État du composant</span><span class="sxs-lookup"><span data-stu-id="200c6-211">?component-state</span></span>       | <span data-ttu-id="200c6-212">Dans la table de [conditions](condition-table.md) et dans les tables de [séquence](using-a-sequence-table.md) , après l’action [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="200c6-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="200c6-213">Le tableau suivant indique les valeurs d’état des fonctionnalités et des composants utilisées dans les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="200c6-214">Ces États ne sont pas définis tant que [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) n’est pas appelé, soit directement, soit par l’action [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="200c6-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="200c6-215">State</span><span class="sxs-lookup"><span data-stu-id="200c6-215">State</span></span>                    | <span data-ttu-id="200c6-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="200c6-216">Value</span></span> | <span data-ttu-id="200c6-217">Signification</span><span class="sxs-lookup"><span data-stu-id="200c6-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="200c6-218">INSTALLSTATE \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="200c6-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="200c6-219">-1</span><span class="sxs-lookup"><span data-stu-id="200c6-219">-1</span></span>    | <span data-ttu-id="200c6-220">Aucune action à effectuer sur la fonctionnalité ou le composant.</span><span class="sxs-lookup"><span data-stu-id="200c6-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="200c6-221">INSTALLSTATE \_ publié</span><span class="sxs-lookup"><span data-stu-id="200c6-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="200c6-222">1</span><span class="sxs-lookup"><span data-stu-id="200c6-222">1</span></span>     | <span data-ttu-id="200c6-223">Fonctionnalité publiée.</span><span class="sxs-lookup"><span data-stu-id="200c6-223">Advertised feature.</span></span> <span data-ttu-id="200c6-224">Cet État n’est pas disponible pour les composants.</span><span class="sxs-lookup"><span data-stu-id="200c6-224">This state is not available for components.</span></span> |
| <span data-ttu-id="200c6-225">INSTALLSTATE \_ absent</span><span class="sxs-lookup"><span data-stu-id="200c6-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="200c6-226">2</span><span class="sxs-lookup"><span data-stu-id="200c6-226">2</span></span>     | <span data-ttu-id="200c6-227">La fonctionnalité ou le composant n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="200c6-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="200c6-228">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="200c6-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="200c6-229">3</span><span class="sxs-lookup"><span data-stu-id="200c6-229">3</span></span>     | <span data-ttu-id="200c6-230">Fonctionnalité ou composant sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="200c6-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="200c6-231">\_source INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="200c6-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="200c6-232">4</span><span class="sxs-lookup"><span data-stu-id="200c6-232">4</span></span>     | <span data-ttu-id="200c6-233">La fonctionnalité ou le composant s’exécutent à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="200c6-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="200c6-234">Par exemple, l’expression conditionnelle « &MyFeature = 3 » prend la valeur true uniquement si MyFeature change de son état actuel à l’état d’installation sur l’ordinateur local, INSTALLSTATE \_ local.</span><span class="sxs-lookup"><span data-stu-id="200c6-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="200c6-235">Notez que vous ne devez pas dépendre de la condition $Component 1 = 3 pour vérifier si Composant1 est installé localement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="200c6-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="200c6-236">Cela peut échouer si Composant1 est installé par plusieurs produits.</span><span class="sxs-lookup"><span data-stu-id="200c6-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="200c6-237">Une fois Composant1 installé localement par product1, le programme d’installation évalue la condition $Component 1 = 3 comme false pendant l’installation de Product2.</span><span class="sxs-lookup"><span data-stu-id="200c6-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="200c6-238">Cela est dû au fait que le programme d’installation détermine la version du composant à l’aide du chemin d’accès de clé du composant et marque le composant pour l’installation si sa version est supérieure ou égale au composant installé.</span><span class="sxs-lookup"><span data-stu-id="200c6-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="200c6-239">Notez que le programme d’installation n’effectuera pas de comparaisons directes du type de données [version](version.md) dans les instructions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="200c6-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="200c6-240">Par exemple, vous ne pouvez pas utiliser des opérateurs comparatifs pour comparer des versions telles que « 01,10 » et « 1,010 » dans une instruction conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="200c6-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="200c6-241">Utilisez plutôt une méthode valide pour rechercher une version, comme décrit dans [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), puis définir une propriété.</span><span class="sxs-lookup"><span data-stu-id="200c6-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="200c6-242">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="200c6-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="200c6-243">Utilisation des propriétés dans les instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="200c6-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



