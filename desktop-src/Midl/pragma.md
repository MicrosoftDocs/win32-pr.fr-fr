---
title: pragma (attribut)
description: La directive \ pragma MIDL \_ echo indique à MIDL d’émettre la chaîne spécifiée, sans les caractères de guillemets, dans le fichier d’en-tête généré.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma, attribut MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940373"
---
# <a name="pragma-attribute"></a><span data-ttu-id="69ee5-104">pragma (attribut)</span><span class="sxs-lookup"><span data-stu-id="69ee5-104">pragma attribute</span></span>

<span data-ttu-id="69ee5-105">La \# directive **pragma MIDL \_ echo** indique à MIDL d’émettre la chaîne spécifiée, sans les caractères de guillemets, dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="69ee5-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="69ee5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69ee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ee5-107">*string*</span><span class="sxs-lookup"><span data-stu-id="69ee5-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="69ee5-108">Spécifie une chaîne insérée dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="69ee5-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="69ee5-109">Les guillemets sont supprimés pendant le processus d’insertion.</span><span class="sxs-lookup"><span data-stu-id="69ee5-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="69ee5-110">*séquence de jetons*</span><span class="sxs-lookup"><span data-stu-id="69ee5-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="69ee5-111">Spécifie une séquence de jetons insérés dans le fichier d’en-tête généré dans le cadre d’une directive **\# pragma** sans traitement par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="69ee5-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="69ee5-112">*n*</span><span class="sxs-lookup"><span data-stu-id="69ee5-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="69ee5-113">Spécifie la taille actuelle du Pack.</span><span class="sxs-lookup"><span data-stu-id="69ee5-113">Specifies the current pack size.</span></span> <span data-ttu-id="69ee5-114">Les valeurs valides sont 1, 2, 4, 8 et 16.</span><span class="sxs-lookup"><span data-stu-id="69ee5-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="69ee5-115">*id*</span><span class="sxs-lookup"><span data-stu-id="69ee5-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="69ee5-116">Spécifie l’identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69ee5-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69ee5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="69ee5-117">Remarks</span></span>

<span data-ttu-id="69ee5-118">Les directives de prétraitement du langage c qui s’affichent dans le fichier IDL sont traitées par le préprocesseur du compilateur C.</span><span class="sxs-lookup"><span data-stu-id="69ee5-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="69ee5-119">Les directives de **\# définition** dans le fichier IDL sont disponibles pendant la compilation MIDL, mais pas pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="69ee5-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="69ee5-120">Par exemple, quand le préprocesseur rencontre la directive « \# définir Windows 4 », le préprocesseur remplace toutes les occurrences de « Windows » dans le fichier IDL par « 4 ».</span><span class="sxs-lookup"><span data-stu-id="69ee5-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="69ee5-121">Le symbole « WINDOWS » n’est pas disponible au moment de la compilation C.</span><span class="sxs-lookup"><span data-stu-id="69ee5-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="69ee5-122">Pour permettre aux définitions de macros de préprocesseur C de passer par le compilateur MIDL au compilateur C, utilisez la directive **\# pragma MIDL \_ echo** ou le [**\_ guillemet RPC**](cpp-quote.md) .</span><span class="sxs-lookup"><span data-stu-id="69ee5-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="69ee5-123">Ces directives indiquent au compilateur MIDL de générer un fichier d’en-tête qui contient la chaîne de paramètre avec les guillemets supprimés.</span><span class="sxs-lookup"><span data-stu-id="69ee5-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="69ee5-124">Les directives **\# pragma MIDL \_ echo** et **CPP des \_ guillemets** sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="69ee5-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="69ee5-125">La directive **\# pragma Pack** est utilisée par le compilateur MIDL pour contrôler le compactage des structures.</span><span class="sxs-lookup"><span data-stu-id="69ee5-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="69ee5-126">Il remplace le commutateur de ligne de commande [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="69ee5-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="69ee5-127">L’option Pack (*n*) définit la taille actuelle du Pack sur une valeur spécifique : 1, 2, 4, 8 ou 16.</span><span class="sxs-lookup"><span data-stu-id="69ee5-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="69ee5-128">Les options Pack (push) et Pack (POP) présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="69ee5-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="69ee5-129">Le compilateur gère une pile de compression.</span><span class="sxs-lookup"><span data-stu-id="69ee5-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="69ee5-130">Les éléments de la pile de compression incluent une taille de Pack et un *ID* facultatif. La pile est limitée uniquement par la mémoire disponible avec la taille de Pack actuelle en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="69ee5-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="69ee5-131">Les résultats de Pack (push) ont fait l’objet d’un push vers la pile de compression.</span><span class="sxs-lookup"><span data-stu-id="69ee5-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="69ee5-132">La pile est limitée par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="69ee5-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="69ee5-133">Pack (push,*n*) est identique à Pack (push) suivi de Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="69ee5-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="69ee5-134">Pack (push, *ID*) envoie également l' *ID* vers la pile de compression avec la taille de Pack.</span><span class="sxs-lookup"><span data-stu-id="69ee5-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="69ee5-135">Pack (push, *ID*, *n*) est identique à Pack (push, *ID*) suivi de Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="69ee5-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="69ee5-136">Pack (POP) génère un pop de la pile de compression.</span><span class="sxs-lookup"><span data-stu-id="69ee5-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="69ee5-137">Les pop déséquilibrés provoquent des avertissements et définissent la taille actuelle du Pack à la valeur de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="69ee5-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="69ee5-138">Si Pack (pop, *ID*, *n*) est spécifié, *n* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="69ee5-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="69ee5-139">Le compilateur MIDL place les chaînes spécifiées dans les directives de [**\\ \_ guillemet**](cpp-quote.md) et de **pragma** cpp dans le fichier d’en-tête dans l’ordre dans lequel elles sont spécifiées dans le fichier IDL et relatives à d’autres composants d’interface dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="69ee5-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="69ee5-140">Les chaînes doivent généralement apparaître dans la section du corps de l’interface du fichier IDL après toutes les opérations d' [**importation**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="69ee5-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="69ee5-141">Le compilateur MIDL ne tente pas de traiter les directives **\# pragma** qui ne commencent pas par le préfixe « MIDL » \_ .</span><span class="sxs-lookup"><span data-stu-id="69ee5-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="69ee5-142">Les autres directives **\# pragma** du fichier IDL sont passées dans le fichier d’en-tête généré sans modification.</span><span class="sxs-lookup"><span data-stu-id="69ee5-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="69ee5-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="69ee5-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="69ee5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69ee5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ee5-145">**\_Devis CPP**</span><span class="sxs-lookup"><span data-stu-id="69ee5-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="69ee5-146">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="69ee5-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="69ee5-147">**port**</span><span class="sxs-lookup"><span data-stu-id="69ee5-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="69ee5-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="69ee5-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




