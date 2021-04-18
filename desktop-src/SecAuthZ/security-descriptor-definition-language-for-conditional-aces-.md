---
description: Une entrée de contrôle d’accès conditionnel (ACE) permet l’évaluation d’une condition d’accès lors de l’exécution d’une vérification d’accès. Le langage SDDL (Security Descriptor Definition Language) fournit la syntaxe permettant de définir des ACE conditionnelles dans un format de chaîne.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Langage de définition du descripteur de sécurité pour les ACE conditionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527015"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="78fe3-104">Langage de définition du descripteur de sécurité pour les ACE conditionnelles</span><span class="sxs-lookup"><span data-stu-id="78fe3-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="78fe3-105">Une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) permet l’évaluation d’une condition d’accès lors de l’exécution d’une vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="78fe3-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="78fe3-106">Le langage SDDL (Security Descriptor Definition Language) fournit la syntaxe permettant de définir des ACE conditionnelles dans un format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="78fe3-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="78fe3-107">Le SDDL pour une entrée du contrôle d’accès conditionnel est le même que pour n’importe quelle entrée du contrôle d’accès, avec la syntaxe de l’instruction conditionnelle ajoutée à la fin de la chaîne ACE.</span><span class="sxs-lookup"><span data-stu-id="78fe3-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="78fe3-108">Pour plus d’informations sur SDDL, consultez [langage de définition du descripteur de sécurité](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="78fe3-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="78fe3-109">Le \# signe « » est synonyme de «0 » dans les attributs de ressource.</span><span class="sxs-lookup"><span data-stu-id="78fe3-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="78fe3-110">Par exemple, D :AI (XA ; OICI ; FA ;;; WD ; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) est équivalent à et interprété comme D :ai (XA ; oici ; FA ;;; WD ; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="78fe3-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="78fe3-111">Format de chaîne ACE conditionnel</span><span class="sxs-lookup"><span data-stu-id="78fe3-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="78fe3-112">Expressions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="78fe3-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="78fe3-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="78fe3-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="78fe3-114">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="78fe3-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="78fe3-115">Priorité des opérateurs</span><span class="sxs-lookup"><span data-stu-id="78fe3-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="78fe3-116">Valeurs inconnues</span><span class="sxs-lookup"><span data-stu-id="78fe3-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="78fe3-117">Évaluation d’entrée de contrôle d’accès conditionnelle</span><span class="sxs-lookup"><span data-stu-id="78fe3-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="78fe3-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="78fe3-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="78fe3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78fe3-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="78fe3-120">Format de chaîne ACE conditionnel</span><span class="sxs-lookup"><span data-stu-id="78fe3-120">Conditional ACE String Format</span></span>

<span data-ttu-id="78fe3-121">Chaque entrée du contrôle d’accès dans une chaîne de [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) est mise entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="78fe3-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="78fe3-122">Les champs de l’entrée du contrôle d’accès sont dans l’ordre suivant et sont séparés par des points-virgules (;).</span><span class="sxs-lookup"><span data-stu-id="78fe3-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="78fe3-123">*AceType ***;** _AceFlags_* _;_ *_Droits_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="78fe3-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="78fe3-124">Les champs sont décrits dans [chaînes ACE](ace-strings.md), avec les exceptions suivantes.</span><span class="sxs-lookup"><span data-stu-id="78fe3-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="78fe3-125">Le champ *AceType* peut être l’une des chaînes suivantes.</span><span class="sxs-lookup"><span data-stu-id="78fe3-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="78fe3-126">Chaîne de type ACE</span><span class="sxs-lookup"><span data-stu-id="78fe3-126">ACE type string</span></span> | <span data-ttu-id="78fe3-127">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="78fe3-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="78fe3-128">Valeur AceType</span><span class="sxs-lookup"><span data-stu-id="78fe3-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="78fe3-129">XA</span><span class="sxs-lookup"><span data-stu-id="78fe3-129">"XA"</span></span><br/> | <span data-ttu-id="78fe3-130">\_ \_ accès au rappel SDDL \_ autorisé</span><span class="sxs-lookup"><span data-stu-id="78fe3-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="78fe3-131">\_type d' \_ entrée du rappel autorisé \_ pour l’accès \_</span><span class="sxs-lookup"><span data-stu-id="78fe3-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="78fe3-132">VERROUILLAGE</span><span class="sxs-lookup"><span data-stu-id="78fe3-132">"XD"</span></span><br/> | <span data-ttu-id="78fe3-133">\_ \_ accès au rappel SDDL \_ refusé</span><span class="sxs-lookup"><span data-stu-id="78fe3-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="78fe3-134">\_type d' \_ ACE de rappel de refus d’accès \_ \_</span><span class="sxs-lookup"><span data-stu-id="78fe3-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="78fe3-135">La chaîne ACE comprend une ou plusieurs expressions conditionnelles, placées entre parenthèses à la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78fe3-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="78fe3-136">Expressions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="78fe3-136">Conditional Expressions</span></span>

<span data-ttu-id="78fe3-137">Une expression conditionnelle peut inclure l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="78fe3-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="78fe3-138">Élément d'expression</span><span class="sxs-lookup"><span data-stu-id="78fe3-138">Expression element</span></span>                                                | <span data-ttu-id="78fe3-139">Description</span><span class="sxs-lookup"><span data-stu-id="78fe3-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fe3-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="78fe3-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="78fe3-141">Teste si l’attribut spécifié a une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="78fe3-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="78fe3-142">**existe** *AttributeName*</span><span class="sxs-lookup"><span data-stu-id="78fe3-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="78fe3-143">Teste si l’attribut spécifié existe dans le contexte client.</span><span class="sxs-lookup"><span data-stu-id="78fe3-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="78fe3-144">*Valeur* de l' *opérateur* *AttributeName*</span><span class="sxs-lookup"><span data-stu-id="78fe3-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="78fe3-145">Retourne le résultat de l’opération spécifiée.</span><span class="sxs-lookup"><span data-stu-id="78fe3-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="78fe3-146">\* ConditionalExpression \* **\|\|** _ConditionalExpression_</span><span class="sxs-lookup"><span data-stu-id="78fe3-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="78fe3-147">Teste si l’une des expressions conditionnelles spécifiées a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="78fe3-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="78fe3-148">*ConditionalExpression* **&&** *ConditionalExpression*</span><span class="sxs-lookup"><span data-stu-id="78fe3-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="78fe3-149">Teste si les deux expressions conditionnelles spécifiées ont la valeur true.</span><span class="sxs-lookup"><span data-stu-id="78fe3-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="78fe3-150">**! (**_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="78fe3-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="78fe3-151">Inverse d’une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="78fe3-152">**Membre \_ de {**_SidArray_*_}_*</span><span class="sxs-lookup"><span data-stu-id="78fe3-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="78fe3-153">Teste si le SID et le tableau d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) du contexte client contient tous les [identificateurs de sécurité](security-identifiers.md) (SID) de la liste séparée par des virgules spécifiée par *SidArray*.</span><span class="sxs-lookup"><span data-stu-id="78fe3-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="78fe3-154">Pour les ACE Allow, le SID du contexte client doit avoir le jeu d’attributs **\_ \_ Enabled Group** pour être considéré comme une correspondance.</span><span class="sxs-lookup"><span data-stu-id="78fe3-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="78fe3-155">Pour les ACE de refus, un SID de contexte client doit avoir le **groupe de se \_ \_ activé** ou le **\_ groupe \_ de se utilisé pour l’attribut \_ de \_ refus \_ uniquement** défini pour être considéré comme une correspondance.</span><span class="sxs-lookup"><span data-stu-id="78fe3-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="78fe3-156">Le tableau *SidArray* peut contenir soit des chaînes sid (par exemple, « S-1-5-6 »), soit des alias sid (par exemple, « BA »).</span><span class="sxs-lookup"><span data-stu-id="78fe3-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="78fe3-157">Attributs</span><span class="sxs-lookup"><span data-stu-id="78fe3-157">Attributes</span></span>

<span data-ttu-id="78fe3-158">Un attribut représente un élément dans le tableau d' [**\_ informations des \_ attributs \_ de sécurité authnt**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) dans le contexte client.</span><span class="sxs-lookup"><span data-stu-id="78fe3-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="78fe3-159">Un nom d’attribut peut contenir des caractères alphanumériques et les caractères «  : », « / », « . » et « \_ ».</span><span class="sxs-lookup"><span data-stu-id="78fe3-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="78fe3-160">Une valeur d’attribut peut être de l’un des types suivants.</span><span class="sxs-lookup"><span data-stu-id="78fe3-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="78fe3-161">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="78fe3-161">Value type</span></span>         | <span data-ttu-id="78fe3-162">Description</span><span class="sxs-lookup"><span data-stu-id="78fe3-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fe3-163">Integer</span><span class="sxs-lookup"><span data-stu-id="78fe3-163">Integer</span></span><br/> | <span data-ttu-id="78fe3-164">Entier 64 bits en notation décimale ou hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="78fe3-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="78fe3-165">String</span><span class="sxs-lookup"><span data-stu-id="78fe3-165">String</span></span><br/>  | <span data-ttu-id="78fe3-166">Valeur de chaîne délimitée par des guillemets.</span><span class="sxs-lookup"><span data-stu-id="78fe3-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="78fe3-167">SID</span><span class="sxs-lookup"><span data-stu-id="78fe3-167">SID</span></span><br/>     | <span data-ttu-id="78fe3-168">SID (S-1-1-0) ou SID (BA).</span><span class="sxs-lookup"><span data-stu-id="78fe3-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="78fe3-169">Doit se trouver sur le RHS du membre \_ de ou de l’appareil \_ membre \_ de.</span><span class="sxs-lookup"><span data-stu-id="78fe3-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="78fe3-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="78fe3-170">BLOB</span></span><br/>    | <span data-ttu-id="78fe3-171">\# suivi de nombres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="78fe3-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="78fe3-172">Si la longueur des nombres est impaire, le \# est converti en 0 pour le faire même.</span><span class="sxs-lookup"><span data-stu-id="78fe3-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="78fe3-173">En outre \# , un autre emplacement dans la valeur est traduit en 0.</span><span class="sxs-lookup"><span data-stu-id="78fe3-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="78fe3-174">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="78fe3-174">Operators</span></span>

<span data-ttu-id="78fe3-175">Les opérateurs suivants sont définis pour une utilisation dans les expressions conditionnelles pour tester les valeurs des attributs.</span><span class="sxs-lookup"><span data-stu-id="78fe3-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="78fe3-176">Il s’agit d’opérateurs binaires et utilisés dans la forme *valeur* de l' *opérateur* *AttributeName* .</span><span class="sxs-lookup"><span data-stu-id="78fe3-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="78fe3-177">Opérateur</span><span class="sxs-lookup"><span data-stu-id="78fe3-177">Operator</span></span>            | <span data-ttu-id="78fe3-178">Description</span><span class="sxs-lookup"><span data-stu-id="78fe3-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="78fe3-179">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="78fe3-180">!=</span><span class="sxs-lookup"><span data-stu-id="78fe3-180">!=</span></span><br/>       | <span data-ttu-id="78fe3-181">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="78fe3-182">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="78fe3-183">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="78fe3-184">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="78fe3-185">Définition conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="78fe3-186">Contient</span><span class="sxs-lookup"><span data-stu-id="78fe3-186">Contains</span></span><br/> | <span data-ttu-id="78fe3-187">**True** si la valeur de l’attribut spécifié est un sur-ensemble de la valeur spécifiée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="78fe3-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="78fe3-188">L’un \_ des</span><span class="sxs-lookup"><span data-stu-id="78fe3-188">Any\_of</span></span><br/>  | <span data-ttu-id="78fe3-189">**True** si la valeur spécifiée est un sur-ensemble de la valeur de l’attribut spécifié ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="78fe3-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="78fe3-190">En outre, les opérateurs unaires existent, les membres \_ et les négations ( !) sont définis comme décrit dans le tableau des expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="78fe3-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="78fe3-191">L’opérateur « Contains » doit être précédé et suivi d’un espace blanc, et l’opérateur « ANY \_ of » doit être précédé d’un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="78fe3-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="78fe3-192">Priorité des opérateurs</span><span class="sxs-lookup"><span data-stu-id="78fe3-192">Operator Precedence</span></span>

<span data-ttu-id="78fe3-193">Les opérateurs sont évalués dans l’ordre de priorité suivant, avec des opérations de priorité égale en cours d’évaluation de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="78fe3-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="78fe3-194">Exists, membre \_ de</span><span class="sxs-lookup"><span data-stu-id="78fe3-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="78fe3-195">Contains, \_ any</span><span class="sxs-lookup"><span data-stu-id="78fe3-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="78fe3-196">= =, ! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="78fe3-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="78fe3-197">!</span><span class="sxs-lookup"><span data-stu-id="78fe3-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="78fe3-198">En outre, toute partie d’une expression conditionnelle peut être placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="78fe3-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="78fe3-199">Les expressions entre parenthèses sont évaluées en premier.</span><span class="sxs-lookup"><span data-stu-id="78fe3-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="78fe3-200">Valeurs inconnues</span><span class="sxs-lookup"><span data-stu-id="78fe3-200">Unknown Values</span></span>

<span data-ttu-id="78fe3-201">Les résultats des expressions conditionnelles renvoient parfois la valeur **Unknown**.</span><span class="sxs-lookup"><span data-stu-id="78fe3-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="78fe3-202">Par exemple, l’une des opérations relationnelles retourne **Unknown** lorsque l’attribut spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="78fe3-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="78fe3-203">Le tableau suivant décrit les résultats d’une opération **and** logique entre deux expressions conditionnelles, *ConditionalExpression1* et *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="78fe3-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="78fe3-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="78fe3-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="78fe3-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="78fe3-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="78fe3-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="78fe3-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="78fe3-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-207">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-208">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="78fe3-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-210">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-211">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-213">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="78fe3-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-216">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-217">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-219">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-220">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-222">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-226">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="78fe3-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-229">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="78fe3-234">Le tableau suivant décrit les résultats d’une opération **or** logique entre deux expressions conditionnelles, *ConditionalExpression1* et *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="78fe3-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="78fe3-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="78fe3-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="78fe3-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="78fe3-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="78fe3-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="78fe3-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="78fe3-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="78fe3-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="78fe3-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-239">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-240">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="78fe3-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-242">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-243">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="78fe3-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-245">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="78fe3-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-248">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-249">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="78fe3-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-251">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-252">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="78fe3-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-254">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-258">**TRUE**</span></span><br/>      | <span data-ttu-id="78fe3-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="78fe3-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="78fe3-261">**FALSE**</span></span><br/>     | <span data-ttu-id="78fe3-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="78fe3-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="78fe3-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="78fe3-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="78fe3-266">La négation d’une expression conditionnelle avec une valeur **Unknown** est également **inconnue**.</span><span class="sxs-lookup"><span data-stu-id="78fe3-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="78fe3-267">Évaluation d’entrée de contrôle d’accès conditionnelle</span><span class="sxs-lookup"><span data-stu-id="78fe3-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="78fe3-268">Le tableau suivant décrit le résultat de la vérification d’accès d’une entrée du contrôle d’accès conditionnel en fonction de l’évaluation finale de l’expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="78fe3-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="78fe3-269">Type d’entrée de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="78fe3-269">ACE type</span></span>         | <span data-ttu-id="78fe3-270">TRUE</span><span class="sxs-lookup"><span data-stu-id="78fe3-270">TRUE</span></span>             | <span data-ttu-id="78fe3-271">FALSE</span><span class="sxs-lookup"><span data-stu-id="78fe3-271">FALSE</span></span>                 | <span data-ttu-id="78fe3-272">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="78fe3-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="78fe3-273">Autoriser</span><span class="sxs-lookup"><span data-stu-id="78fe3-273">Allow</span></span><br/> | <span data-ttu-id="78fe3-274">Autoriser</span><span class="sxs-lookup"><span data-stu-id="78fe3-274">Allow</span></span><br/> | <span data-ttu-id="78fe3-275">Ignorer l’ACE</span><span class="sxs-lookup"><span data-stu-id="78fe3-275">Ignore ACE</span></span><br/> | <span data-ttu-id="78fe3-276">Ignorer l’ACE</span><span class="sxs-lookup"><span data-stu-id="78fe3-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="78fe3-277">Deny</span><span class="sxs-lookup"><span data-stu-id="78fe3-277">Deny</span></span><br/>  | <span data-ttu-id="78fe3-278">Deny</span><span class="sxs-lookup"><span data-stu-id="78fe3-278">Deny</span></span><br/>  | <span data-ttu-id="78fe3-279">Ignorer l’ACE</span><span class="sxs-lookup"><span data-stu-id="78fe3-279">Ignore ACE</span></span><br/> | <span data-ttu-id="78fe3-280">Deny</span><span class="sxs-lookup"><span data-stu-id="78fe3-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="78fe3-281">Exemples</span><span class="sxs-lookup"><span data-stu-id="78fe3-281">Examples</span></span>

<span data-ttu-id="78fe3-282">Les exemples suivants montrent comment les stratégies d’accès spécifiées sont représentées par une entrée de contrôle d’accès conditionnel définie à l’aide du langage SDDL.</span><span class="sxs-lookup"><span data-stu-id="78fe3-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="78fe3-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi</span><span class="sxs-lookup"><span data-stu-id="78fe3-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-284">Autoriser l’exécution à tout le monde si les deux conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="78fe3-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="78fe3-285">Titre = PM</span><span class="sxs-lookup"><span data-stu-id="78fe3-285">Title = PM</span></span>
-   <span data-ttu-id="78fe3-286">Division = finance ou division = ventes</span><span class="sxs-lookup"><span data-stu-id="78fe3-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="78fe3-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="78fe3-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-288">D : (XA ;; FX ;;; S-1-1-0 ; ( @User.Title = = "PM"  &&  ( @User.Division = = "finance" \| \| @User.Division = = "Sales")))</span><span class="sxs-lookup"><span data-stu-id="78fe3-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="78fe3-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi</span><span class="sxs-lookup"><span data-stu-id="78fe3-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-290">Autorisez l’exécution si l’un des projets de l’utilisateur s’entrecoupent avec les projets de fichier s.</span><span class="sxs-lookup"><span data-stu-id="78fe3-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="78fe3-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="78fe3-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-292">D : (XA ;; FX ;;; S-1-1-0 ; ( @User.Project Tout \_ @Resource.Project ))</span><span class="sxs-lookup"><span data-stu-id="78fe3-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="78fe3-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi</span><span class="sxs-lookup"><span data-stu-id="78fe3-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-294">Autoriser l’accès en lecture si l’utilisateur s’est connecté avec une carte à puce, est un opérateur de sauvegarde et se connecte à partir d’un ordinateur sur lequel BitLocker est activé.</span><span class="sxs-lookup"><span data-stu-id="78fe3-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="78fe3-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="78fe3-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="78fe3-296">D : (XA ;; FR ;;; S-1-1-0 ; (Membre \_ de {sid (SID de carte à puce \_ ), sid (BO)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="78fe3-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="78fe3-297">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78fe3-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="78fe3-298">[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="78fe3-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

