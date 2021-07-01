---
title: Grammaire
description: Les instructions HLSL sont construites à l’aide des règles suivantes pour la grammaire.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129847"
---
# <a name="grammar"></a><span data-ttu-id="a4e97-103">Grammaire</span><span class="sxs-lookup"><span data-stu-id="a4e97-103">Grammar</span></span>

<span data-ttu-id="a4e97-104">Les instructions HLSL sont construites à l’aide des règles suivantes pour la grammaire.</span><span class="sxs-lookup"><span data-stu-id="a4e97-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="a4e97-105">Espace blanc</span><span class="sxs-lookup"><span data-stu-id="a4e97-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="a4e97-106">Nombres à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="a4e97-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="a4e97-107">Nombres entiers</span><span class="sxs-lookup"><span data-stu-id="a4e97-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="a4e97-108">Caractères</span><span class="sxs-lookup"><span data-stu-id="a4e97-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="a4e97-109">Chaînes</span><span class="sxs-lookup"><span data-stu-id="a4e97-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="a4e97-110">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="a4e97-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="a4e97-111">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="a4e97-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="a4e97-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4e97-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="a4e97-113">Espace blanc</span><span class="sxs-lookup"><span data-stu-id="a4e97-113">Whitespace</span></span>

<span data-ttu-id="a4e97-114">Les caractères suivants sont reconnus comme des espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="a4e97-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="a4e97-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="a4e97-115">SPACE</span></span>
- <span data-ttu-id="a4e97-116">Tab</span><span class="sxs-lookup"><span data-stu-id="a4e97-116">TAB</span></span>
- <span data-ttu-id="a4e97-117">ÉCHÉANCE</span><span class="sxs-lookup"><span data-stu-id="a4e97-117">EOL</span></span>
- <span data-ttu-id="a4e97-118">Commentaires de style C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="a4e97-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="a4e97-119">Commentaires de style C++ (//)</span><span class="sxs-lookup"><span data-stu-id="a4e97-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="a4e97-120">Nombres à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="a4e97-120">Floating point numbers</span></span>

<span data-ttu-id="a4e97-121">Les nombres à virgule flottante sont représentés en langage HLSL comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e97-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="a4e97-122">fraction-constante de l’exposant-partie (opt)-suffixe à virgule flottante (opt)</span><span class="sxs-lookup"><span data-stu-id="a4e97-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="a4e97-123">digit-Sequence-suffixe à virgule flottante de partie exposant (opt)</span><span class="sxs-lookup"><span data-stu-id="a4e97-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="a4e97-124">fraction-constante :</span><span class="sxs-lookup"><span data-stu-id="a4e97-124">fractional-constant :</span></span>

    <span data-ttu-id="a4e97-125">chiffre-séquence (opt).</span><span class="sxs-lookup"><span data-stu-id="a4e97-125">digit-sequence(opt) .</span></span> <span data-ttu-id="a4e97-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="a4e97-126">digit-sequence</span></span>

    <span data-ttu-id="a4e97-127">chiffre-séquence.</span><span class="sxs-lookup"><span data-stu-id="a4e97-127">digit-sequence .</span></span>

-   <span data-ttu-id="a4e97-128">partie exposant :</span><span class="sxs-lookup"><span data-stu-id="a4e97-128">exponent-part :</span></span>

    <span data-ttu-id="a4e97-129">chiffre e (opt)-séquence</span><span class="sxs-lookup"><span data-stu-id="a4e97-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="a4e97-130">Chiffre E (opt)-séquence</span><span class="sxs-lookup"><span data-stu-id="a4e97-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="a4e97-131">sign : un des éléments suivants</span><span class="sxs-lookup"><span data-stu-id="a4e97-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="a4e97-132">chiffre-séquence :</span><span class="sxs-lookup"><span data-stu-id="a4e97-132">digit-sequence :</span></span>

    <span data-ttu-id="a4e97-133">digit</span><span class="sxs-lookup"><span data-stu-id="a4e97-133">digit</span></span>

    <span data-ttu-id="a4e97-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="a4e97-134">digit-sequence digit</span></span>

-   <span data-ttu-id="a4e97-135">floating-suffix : un des éléments suivants</span><span class="sxs-lookup"><span data-stu-id="a4e97-135">floating-suffix : one of</span></span>

    <span data-ttu-id="a4e97-136">h H f F l</span><span class="sxs-lookup"><span data-stu-id="a4e97-136">h H f F l L</span></span>

    <span data-ttu-id="a4e97-137">Utilisez le suffixe « L » pour spécifier un littéral à virgule flottante de précision 64 bits complet.</span><span class="sxs-lookup"><span data-stu-id="a4e97-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="a4e97-138">Un littéral de virgule flottante de 32 bits est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a4e97-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="a4e97-139">Par exemple, le compilateur reconnaît la valeur littérale suivante comme un littéral à virgule flottante de précision 32 bits et ignore les bits inférieurs :</span><span class="sxs-lookup"><span data-stu-id="a4e97-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="a4e97-140">Le compilateur reconnaît la valeur littérale suivante comme un littéral à virgule flottante de précision 64 bits :</span><span class="sxs-lookup"><span data-stu-id="a4e97-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="a4e97-141">Nombres entiers</span><span class="sxs-lookup"><span data-stu-id="a4e97-141">Integer numbers</span></span>

<span data-ttu-id="a4e97-142">Les nombres entiers sont représentés en langage HLSL comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e97-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="a4e97-143">entier-constante entier-suffixe (opt)</span><span class="sxs-lookup"><span data-stu-id="a4e97-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="a4e97-144">Integer-constante : un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4e97-144">integer-constant: one of</span></span>

    <span data-ttu-id="a4e97-145">\# (nombre décimal)</span><span class="sxs-lookup"><span data-stu-id="a4e97-145">\# (decimal number)</span></span>

    <span data-ttu-id="a4e97-146">0 \# (nombre octal)</span><span class="sxs-lookup"><span data-stu-id="a4e97-146">0\# (octal number)</span></span>

    <span data-ttu-id="a4e97-147">0x \# (nombre hexadécimal)</span><span class="sxs-lookup"><span data-stu-id="a4e97-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="a4e97-148">le suffixe entier peut être l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4e97-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="a4e97-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="a4e97-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="a4e97-150">Caractères</span><span class="sxs-lookup"><span data-stu-id="a4e97-150">Characters</span></span>

<span data-ttu-id="a4e97-151">Les caractères sont représentés en langage HLSL comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e97-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="a4e97-152">Caractère</span><span class="sxs-lookup"><span data-stu-id="a4e97-152">Character</span></span>                                          | <span data-ttu-id="a4e97-153">Description</span><span class="sxs-lookup"><span data-stu-id="a4e97-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="a4e97-154">« c »</span><span class="sxs-lookup"><span data-stu-id="a4e97-154">'c'</span></span>                                       | <span data-ttu-id="a4e97-155">symbole</span><span class="sxs-lookup"><span data-stu-id="a4e97-155">(character)</span></span>                                                     |
| <span data-ttu-id="a4e97-156">' \\ a' ' \\ b' ' \\ f' ' \\ b' ' \\ r' ' \\ t' ' \\ v'</span><span class="sxs-lookup"><span data-stu-id="a4e97-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="a4e97-157">d’échappement</span><span class="sxs-lookup"><span data-stu-id="a4e97-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="a4e97-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="a4e97-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="a4e97-159">(échappement octal, chacun \# est un chiffre octal)</span><span class="sxs-lookup"><span data-stu-id="a4e97-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="a4e97-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="a4e97-160">'\\x\#'</span></span>                                   | <span data-ttu-id="a4e97-161">(caractère d’échappement hexadécimal, \# est un nombre hexadécimal, un nombre quelconque de chiffres)</span><span class="sxs-lookup"><span data-stu-id="a4e97-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="a4e97-162">' \\ c'</span><span class="sxs-lookup"><span data-stu-id="a4e97-162">'\\c'</span></span>                                     | <span data-ttu-id="a4e97-163">(c est un autre caractère, y compris une barre oblique inverse et des guillemets)</span><span class="sxs-lookup"><span data-stu-id="a4e97-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="a4e97-164">Les séquences d’échappement ne sont pas prises en charge dans les expressions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="a4e97-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="a4e97-165">Chaînes</span><span class="sxs-lookup"><span data-stu-id="a4e97-165">Strings</span></span>

<span data-ttu-id="a4e97-166">Les chaînes sont représentées en langage HLSL comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e97-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="a4e97-167">« s » (s est une chaîne avec échappements).</span><span class="sxs-lookup"><span data-stu-id="a4e97-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="a4e97-168">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="a4e97-168">Identifiers</span></span>

<span data-ttu-id="a4e97-169">Les identificateurs sont représentés en langage HLSL comme suit :</span><span class="sxs-lookup"><span data-stu-id="a4e97-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="a4e97-170">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="a4e97-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="a4e97-171">Également tout autre caractère unique qui ne correspondait pas à une autre règle.</span><span class="sxs-lookup"><span data-stu-id="a4e97-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4e97-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4e97-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e97-173">Annexe (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a4e97-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




