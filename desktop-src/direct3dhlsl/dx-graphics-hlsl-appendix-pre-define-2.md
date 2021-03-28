---
title: '\#define, directive (macro)'
description: Directive de préprocesseur qui crée une macro de type fonction.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104990861"
---
# <a name="define-directive-macro"></a><span data-ttu-id="20eb7-103">\#define, directive (macro)</span><span class="sxs-lookup"><span data-stu-id="20eb7-103">\#define directive (macro)</span></span>

<span data-ttu-id="20eb7-104">Directive de préprocesseur qui crée une macro de type fonction.</span><span class="sxs-lookup"><span data-stu-id="20eb7-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="20eb7-105">\#définir l' *identificateur*( *argument0*,..., *argumentN-1* ) *-chaîne de jeton*</span><span class="sxs-lookup"><span data-stu-id="20eb7-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="20eb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20eb7-106">Parameters</span></span>



| <span data-ttu-id="20eb7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="20eb7-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="20eb7-108">Description</span><span class="sxs-lookup"><span data-stu-id="20eb7-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20eb7-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*</span><span class="sxs-lookup"><span data-stu-id="20eb7-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="20eb7-110">Identificateur de la macro.</span><span class="sxs-lookup"><span data-stu-id="20eb7-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="20eb7-111">Une deuxième [ \# définition](dx-graphics-hlsl-appendix-pre-define.md) pour une macro avec un identificateur qui existe déjà dans le contexte actuel génère une erreur, à moins que la deuxième séquence de jeton soit identique à la première.</span><span class="sxs-lookup"><span data-stu-id="20eb7-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="20eb7-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentN-1* )</span><span class="sxs-lookup"><span data-stu-id="20eb7-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="20eb7-113">Liste d’arguments pour la macro.</span><span class="sxs-lookup"><span data-stu-id="20eb7-113">List of arguments to the macro.</span></span> <span data-ttu-id="20eb7-114">La liste d’arguments est délimitée par des virgules, peut être de n’importe quelle longueur et doit être placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="20eb7-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="20eb7-115">Chaque nom d’argument dans la liste doit être unique.</span><span class="sxs-lookup"><span data-stu-id="20eb7-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="20eb7-116">Aucun espace blanc ne peut séparer le paramètre d' *identificateur* et la parenthèse ouvrante.</span><span class="sxs-lookup"><span data-stu-id="20eb7-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="20eb7-117">Utiliser la concaténation de ligne Placez une barre oblique inverse ( \) juste avant le caractère de saut de ligne pour fractionner les directives longues en plusieurs lignes sources.</span><span class="sxs-lookup"><span data-stu-id="20eb7-117">Use line concatenation place a backslash (\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="20eb7-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*jeton-chaîne* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20eb7-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="20eb7-119">Valeur de la macro.</span><span class="sxs-lookup"><span data-stu-id="20eb7-119">Value of the macro.</span></span> <span data-ttu-id="20eb7-120">Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes.</span><span class="sxs-lookup"><span data-stu-id="20eb7-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="20eb7-121">Un ou plusieurs espaces blancs doivent séparer ce paramètre du paramètre *identificateur* ; Cet espace blanc n’est pas considéré comme faisant partie du texte substitué, et n’est pas un espace blanc qui suit le dernier jeton du texte.</span><span class="sxs-lookup"><span data-stu-id="20eb7-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="20eb7-122">Utilisez des parenthèses pour vous assurer que les arguments complexes sont interprétés correctement.</span><span class="sxs-lookup"><span data-stu-id="20eb7-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="20eb7-123">Si la valeur du paramètre *identificateur* est comprise dans le paramètre de *chaîne de jeton* (même suite à une autre expansion macro), il n’est pas développé.</span><span class="sxs-lookup"><span data-stu-id="20eb7-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="20eb7-124">Si vous excluez ce paramètre, toutes les instances du paramètre d' *identificateur* sont supprimées du fichier source.</span><span class="sxs-lookup"><span data-stu-id="20eb7-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="20eb7-125">L’identificateur reste défini et peut être testé à l’aide des directives [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef et \# ifndef définies.</span><span class="sxs-lookup"><span data-stu-id="20eb7-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="20eb7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="20eb7-126">Remarks</span></span>

<span data-ttu-id="20eb7-127">Toutes les instances du paramètre d' *identificateur* qui se produisent après la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) dans le fichier source constituent un appel de macro, et l’identificateur est remplacé par une version du paramètre de *chaîne de jeton* dont les arguments réels sont remplacés par des paramètres formels.</span><span class="sxs-lookup"><span data-stu-id="20eb7-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="20eb7-128">Le nombre de paramètres dans l’appel doit correspondre au nombre de paramètres dans la définition de macro.</span><span class="sxs-lookup"><span data-stu-id="20eb7-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="20eb7-129">L’identificateur est remplacé uniquement lorsqu’il forme un jeton. par exemple, l’identificateur n’est pas remplacé s’il apparaît dans un commentaire, dans une chaîne ou dans le cadre d’un identificateur plus long.</span><span class="sxs-lookup"><span data-stu-id="20eb7-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="20eb7-130">La directive [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indique au préprocesseur d’oublier la définition d’un identificateur. pour plus d’informations, consultez \# directive undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="20eb7-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="20eb7-131">La définition de constantes avec l’option de compilateur/D a le même effet que l’utilisation de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) au début de votre fichier.</span><span class="sxs-lookup"><span data-stu-id="20eb7-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="20eb7-132">Jusqu’à 30 macros peuvent être définies avec l’option/D.</span><span class="sxs-lookup"><span data-stu-id="20eb7-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="20eb7-133">Les arguments réels dans l’appel de macro sont mis en correspondance avec les arguments formels correspondants dans la définition de macro.</span><span class="sxs-lookup"><span data-stu-id="20eb7-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="20eb7-134">Chaque argument formel dans la chaîne de jeton est remplacé par l’argument réel correspondant, à moins que l’argument ne soit précédé d’un \# opérateur String (), Charing ( \# @) ou de collage de jeton ( \# \# ), ou qu’il soit suivi d’un \# \# opérateur.</span><span class="sxs-lookup"><span data-stu-id="20eb7-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="20eb7-135">Toutes les macros figurant dans l'argument réel sont développées avant que la directive ne remplace le paramètre formel.</span><span class="sxs-lookup"><span data-stu-id="20eb7-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="20eb7-136">Le collage de jetons dans le compilateur HLSL est légèrement différent du collage de jeton dans le compilateur C, en ce que les jetons collés doivent être eux-mêmes des jetons valides.</span><span class="sxs-lookup"><span data-stu-id="20eb7-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="20eb7-137">Par exemple, considérez la définition de macro suivante :</span><span class="sxs-lookup"><span data-stu-id="20eb7-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="20eb7-138">Dans le compilateur C, les résultats sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="20eb7-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="20eb7-139">Toutefois, dans le compilateur HLSL, les résultats sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="20eb7-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="20eb7-140">Vous pouvez contourner ce comportement en utilisant la définition de macro suivante à la place.</span><span class="sxs-lookup"><span data-stu-id="20eb7-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="20eb7-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="20eb7-141">Examples</span></span>

<span data-ttu-id="20eb7-142">L’exemple suivant utilise une macro pour définir des lignes de curseur.</span><span class="sxs-lookup"><span data-stu-id="20eb7-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="20eb7-143">L’exemple suivant définit une macro qui récupère un entier Pseudo-aléatoire dans la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20eb7-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="20eb7-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20eb7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20eb7-145">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20eb7-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="20eb7-146">\#définir des surcharges</span><span class="sxs-lookup"><span data-stu-id="20eb7-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="20eb7-147">\#undef, directive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20eb7-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





