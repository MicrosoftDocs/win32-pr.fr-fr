---
title: " Directives if, Elif, Else et endif"
description: Directives de préprocesseur qui contrôlent la compilation des parties d’un fichier source.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Directives HLSL, if, Elif, Else et endif
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101660"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="76e23-104">\#Directives if, \# Elif, \# else et \# endif</span><span class="sxs-lookup"><span data-stu-id="76e23-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="76e23-105">Directives de préprocesseur qui contrôlent la compilation des parties d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="76e23-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="76e23-106">\#Si *ifCondition* ...</span><span class="sxs-lookup"><span data-stu-id="76e23-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="76e23-107">\[\#*elifCondition* elif...\]</span><span class="sxs-lookup"><span data-stu-id="76e23-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="76e23-108">\[\#sinon...\]</span><span class="sxs-lookup"><span data-stu-id="76e23-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="76e23-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="76e23-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="76e23-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76e23-110">Parameters</span></span>



| <span data-ttu-id="76e23-111">Élément</span><span class="sxs-lookup"><span data-stu-id="76e23-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="76e23-112">Description</span><span class="sxs-lookup"><span data-stu-id="76e23-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e23-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span><span class="sxs-lookup"><span data-stu-id="76e23-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="76e23-114">Condition principale à évaluer.</span><span class="sxs-lookup"><span data-stu-id="76e23-114">Primary condition to evaluate.</span></span> <span data-ttu-id="76e23-115">Si ce paramètre a une valeur différente de zéro, tout le texte entre cette \# directive if et l’instance suivante de la \# directive Elif, \# else ou \# endif est conservé dans l’unité de traduction ; sinon, le code source suivant n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="76e23-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="76e23-116">La condition peut utiliser l’opérateur de préprocesseur défini pour déterminer si une constante ou une macro de préprocesseur spécifique est définie ; cette utilisation est équivalente à l’utilisation de la directive [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="76e23-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="76e23-117">Consultez la section Notes pour connaître les restrictions relatives à la valeur du paramètre *ifCondition* .</span><span class="sxs-lookup"><span data-stu-id="76e23-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="76e23-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="76e23-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="76e23-119">Autre condition à évaluer.</span><span class="sxs-lookup"><span data-stu-id="76e23-119">Other condition to evaluate.</span></span> <span data-ttu-id="76e23-120">Si le paramètre *ifCondition* et toutes les \# directives Elif précédentes ont la valeur zéro et que ce paramètre a une valeur différente de zéro, tout le texte entre cette \# directive elif et l’instance suivante de la \# directive Elif, \# else ou \# endif est conservé dans l’unité de traduction ; sinon, le code source suivant n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="76e23-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="76e23-121">La condition peut utiliser l’opérateur de préprocesseur défini pour déterminer si une constante ou une macro de préprocesseur spécifique est définie ; cette utilisation est équivalente à l’utilisation de la directive [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="76e23-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="76e23-122">Consultez la section Notes pour connaître les restrictions relatives à la valeur du paramètre *elifCondition* .</span><span class="sxs-lookup"><span data-stu-id="76e23-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="76e23-123">Notes</span><span class="sxs-lookup"><span data-stu-id="76e23-123">Remarks</span></span>

<span data-ttu-id="76e23-124">Chaque \# directive if dans un fichier source doit être mise en correspondance par une \# directive de fermeture endif.</span><span class="sxs-lookup"><span data-stu-id="76e23-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="76e23-125">Un nombre quelconque de \# directives Elif peuvent apparaître entre les \# directives if et \# endif, mais au plus une \# directive else est autorisée.</span><span class="sxs-lookup"><span data-stu-id="76e23-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="76e23-126">La \# directive else, le cas échéant, doit être la dernière directive avant \# endif.</span><span class="sxs-lookup"><span data-stu-id="76e23-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="76e23-127">Les directives de compilation conditionnelle contenues dans les fichiers include doivent respecter les mêmes conditions.</span><span class="sxs-lookup"><span data-stu-id="76e23-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="76e23-128">Les \# directives if, \# Elif, \# else et \# endif peuvent s’imbriquer dans les parties de texte d’autres \# directives if.</span><span class="sxs-lookup"><span data-stu-id="76e23-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="76e23-129">Chaque \# directive else, \# Elif ou endif imbriquée \# appartient à la directive if précédente la plus proche \# .</span><span class="sxs-lookup"><span data-stu-id="76e23-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="76e23-130">Si aucune condition n’est évaluée à une valeur différente de zéro, le préprocesseur sélectionne le bloc de texte après la \# directive else.</span><span class="sxs-lookup"><span data-stu-id="76e23-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="76e23-131">Si la \# clause else est omise et qu’aucune condition n’est évaluée à une valeur différente de zéro, aucun bloc de texte n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="76e23-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="76e23-132">Les paramètres *ifCondition* et *elifCondition* répondent en grande partie aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="76e23-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="76e23-133">Les expressions de compilation conditionnelles sont traitées comme des valeurs [**longues signées**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) , et ces expressions sont évaluées à l’aide des mêmes règles que les expressions en C++.</span><span class="sxs-lookup"><span data-stu-id="76e23-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="76e23-134">Les expressions doivent être de type intégral et ne peuvent inclure que des constantes entières, des constantes caractère et l'opérateur defined.</span><span class="sxs-lookup"><span data-stu-id="76e23-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="76e23-135">Les expressions ne peuvent pas utiliser **sizeof** ou un opérateur de cast de type.</span><span class="sxs-lookup"><span data-stu-id="76e23-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="76e23-136">Il se peut que l'environnement cible ne puisse pas représenter toutes les plages d'entiers.</span><span class="sxs-lookup"><span data-stu-id="76e23-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="76e23-137">La traduction représente le type [**int**](/windows/desktop/WinProg/windows-data-types) identique au type **long**, et [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) identique à **unsigned long**.</span><span class="sxs-lookup"><span data-stu-id="76e23-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="76e23-138">Le traducteur peut traduire les constantes caractère en un ensemble de valeurs de code différentes de l'ensemble de l'environnement cible.</span><span class="sxs-lookup"><span data-stu-id="76e23-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="76e23-139">Pour déterminer les propriétés de l'environnement cible, vérifiez les valeurs des macros de LIMITS.H dans une application développée pour l'environnement cible.</span><span class="sxs-lookup"><span data-stu-id="76e23-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="76e23-140">L'expression ne doit effectuer aucune interrogation de l'environnement et doit rester isolée par rapport aux détails d'implémentation sur l'ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="76e23-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="76e23-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="76e23-141">Examples</span></span>

<span data-ttu-id="76e23-142">Cette section contient des exemples qui montrent comment utiliser les directives de préprocesseur de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="76e23-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="76e23-143">Utilisation de l’opérateur défini</span><span class="sxs-lookup"><span data-stu-id="76e23-143">Use of the defined operator</span></span>

<span data-ttu-id="76e23-144">L’exemple suivant illustre l’utilisation de l’opérateur défini.</span><span class="sxs-lookup"><span data-stu-id="76e23-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="76e23-145">Si le crédit d’identificateur est défini, l’appel à la fonction de **crédit** est compilé.</span><span class="sxs-lookup"><span data-stu-id="76e23-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="76e23-146">Si le débit de l’identificateur est défini, l’appel à la fonction **Debit** est compilé.</span><span class="sxs-lookup"><span data-stu-id="76e23-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="76e23-147">Si aucun identificateur n’est défini, l’appel à la fonction **printerror** est compilé.</span><span class="sxs-lookup"><span data-stu-id="76e23-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="76e23-148">Notez que « CREDIT » et « Credit » sont des identificateurs distincts en C et C++, car leurs cas sont différents.</span><span class="sxs-lookup"><span data-stu-id="76e23-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="76e23-149">Utilisation des \# directives if imbriquées</span><span class="sxs-lookup"><span data-stu-id="76e23-149">Use of nested \#if directives</span></span>

<span data-ttu-id="76e23-150">L’exemple suivant montre comment imbriquer des \# directives if.</span><span class="sxs-lookup"><span data-stu-id="76e23-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="76e23-151">Cet exemple suppose qu’une constante symbolique nommée DLEVEL a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="76e23-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="76e23-152">Les \# directives elif et \# else sont utilisées pour effectuer l’un des quatre choix, en fonction de la valeur de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="76e23-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="76e23-153">La pile constante est définie sur 0, 100 ou 200, selon la définition de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="76e23-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="76e23-154">Si DLEVEL est supérieur à 5, STACK n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="76e23-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="76e23-155">Utiliser pour inclure des fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="76e23-155">Use for including header files</span></span>

<span data-ttu-id="76e23-156">Une utilisation courante de la compilation conditionnelle consiste à empêcher plusieurs inclusions du même fichier d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="76e23-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="76e23-157">En C++, où les classes sont souvent définies dans les fichiers d’en-tête, les constructions de compilation conditionnelle peuvent être utilisées pour empêcher plusieurs définitions.</span><span class="sxs-lookup"><span data-stu-id="76e23-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="76e23-158">L’exemple suivant détermine si l’exemple de constante symbolique \_ H est défini.</span><span class="sxs-lookup"><span data-stu-id="76e23-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="76e23-159">Dans ce cas, le fichier a déjà été inclus et n’a pas besoin d’être retraité ; Si ce n’est pas le cas, l’exemple \_ de constante H est défini pour indiquer cet exemple. H a déjà été traité.</span><span class="sxs-lookup"><span data-stu-id="76e23-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="76e23-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76e23-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e23-161">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76e23-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

