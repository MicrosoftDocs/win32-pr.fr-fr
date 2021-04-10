---
title: commutateur/char
description: Le commutateur/char permet de s’assurer que le compilateur MIDL et le compilateur C fonctionnent ensemble correctement pour tous les types char et Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- MIDL du commutateur/char
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678669"
---
# <a name="char-switch"></a><span data-ttu-id="1a72f-104">commutateur/char</span><span class="sxs-lookup"><span data-stu-id="1a72f-104">/char switch</span></span>

<span data-ttu-id="1a72f-105">Le commutateur **/char** permet de s’assurer que le compilateur MIDL et le compilateur C fonctionnent ensemble correctement pour tous les types [**char**](char-idl.md) et [**Small**](small.md) .</span><span class="sxs-lookup"><span data-stu-id="1a72f-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="1a72f-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1a72f-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="1a72f-107"><span id="signed"></span><span id="SIGNED"></span>signé \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1a72f-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1a72f-108">Spécifie que le type de compilateur C par défaut pour [**char**](char-idl.md) est signé.</span><span class="sxs-lookup"><span data-stu-id="1a72f-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="1a72f-109">Toutes les occurrences de **char** non accompagnées d’une spécification de signe sont générées en tant que type unsigned char.</span><span class="sxs-lookup"><span data-stu-id="1a72f-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="1a72f-110"><span id="unsigned"></span><span id="UNSIGNED"></span>non signé \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1a72f-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1a72f-111">Spécifie que le type de compilateur C par défaut pour [**char**](char-idl.md) n’est pas signé.</span><span class="sxs-lookup"><span data-stu-id="1a72f-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="1a72f-112">Toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe sont générées comme étant signées petit.</span><span class="sxs-lookup"><span data-stu-id="1a72f-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="1a72f-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1a72f-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1a72f-114">Spécifie que toutes les valeurs [**char**](char-idl.md) doivent être passées dans les fichiers générés sans un mot clé Sign spécifique.</span><span class="sxs-lookup"><span data-stu-id="1a72f-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="1a72f-115">Toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe sont générées sous une forme **réduite**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a72f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1a72f-116">Remarks</span></span>

<span data-ttu-id="1a72f-117">Par définition, le [**caractère**](char-idl.md) MIDL n’est pas signé.</span><span class="sxs-lookup"><span data-stu-id="1a72f-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="1a72f-118">« Small » est défini en termes de **char** ( \# define Small Char) et MIDL [**Small**](small.md) est signé.</span><span class="sxs-lookup"><span data-stu-id="1a72f-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="1a72f-119">Le commutateur **/char** indique au compilateur MIDL de spécifier des déclarations [**signées**](signed.md) ou [**non**](unsigned.md) signées explicites dans les fichiers générés lorsque la déclaration de signe du compilateur C est en conflit avec la valeur par défaut MIDL pour ce type.</span><span class="sxs-lookup"><span data-stu-id="1a72f-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="1a72f-120">N’oubliez pas que le compilateur MIDL génère les stubs en tant que code source C, que vous devez compiler dans le cadre de vos programmes client et serveur.</span><span class="sxs-lookup"><span data-stu-id="1a72f-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="1a72f-121">Certains compilateurs utilisent [**des données de type char**](char-idl.md) partout **signées** , qui sont spécifiées dans le code source.</span><span class="sxs-lookup"><span data-stu-id="1a72f-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="1a72f-122">Le code source stub généré par le compilateur MIDL traite toutes les données **char** comme des **caractères non signés**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="1a72f-123">Si le compilateur MIDL a simplement généré toutes les données **char** dans le fichier IDL en tant que données **char** dans les stubs, les compilateurs qui utilisent un **char signé** pour les données **char** provoqueraient un conflit dans le code source du stub.</span><span class="sxs-lookup"><span data-stu-id="1a72f-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="1a72f-124">L’objectif du commutateur de ligne de commande **/char** est de résoudre ces conflits potentiels.</span><span class="sxs-lookup"><span data-stu-id="1a72f-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="1a72f-125">Elle conserve toutes les données spécifiées en tant que [**char**](char-idl.md) dans le fichier IDL en tant que **unsigned char** dans le code source stub.</span><span class="sxs-lookup"><span data-stu-id="1a72f-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="1a72f-126">Il gère également les [**petites**](small.md) données comme étant signées.</span><span class="sxs-lookup"><span data-stu-id="1a72f-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="1a72f-127">Le tableau suivant récapitule les types générés.</span><span class="sxs-lookup"><span data-stu-id="1a72f-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="1a72f-128">MIDL (option/char)</span><span class="sxs-lookup"><span data-stu-id="1a72f-128">midl /char option</span></span>       | <span data-ttu-id="1a72f-129">Type char généré</span><span class="sxs-lookup"><span data-stu-id="1a72f-129">Generated char type</span></span> | <span data-ttu-id="1a72f-130">Type de petite taille généré</span><span class="sxs-lookup"><span data-stu-id="1a72f-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="1a72f-131">**MIDL/char signé**</span><span class="sxs-lookup"><span data-stu-id="1a72f-131">**midl /char signed**</span></span>   | <span data-ttu-id="1a72f-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="1a72f-132">**unsigned char**</span></span>   | <span data-ttu-id="1a72f-133">**small**</span><span class="sxs-lookup"><span data-stu-id="1a72f-133">**small**</span></span>            |
| <span data-ttu-id="1a72f-134">**MIDL/char non signé**</span><span class="sxs-lookup"><span data-stu-id="1a72f-134">**midl /char unsigned**</span></span> | <span data-ttu-id="1a72f-135">**char**</span><span class="sxs-lookup"><span data-stu-id="1a72f-135">**char**</span></span>            | <span data-ttu-id="1a72f-136">**signé petit**</span><span class="sxs-lookup"><span data-stu-id="1a72f-136">**signed small**</span></span>     |
| <span data-ttu-id="1a72f-137">**MIDL/char ascii7**</span><span class="sxs-lookup"><span data-stu-id="1a72f-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="1a72f-138">**char**</span><span class="sxs-lookup"><span data-stu-id="1a72f-138">**char**</span></span>            | <span data-ttu-id="1a72f-139">**small**</span><span class="sxs-lookup"><span data-stu-id="1a72f-139">**small**</span></span>            |



 

<span data-ttu-id="1a72f-140">L’option **/char** signed indique que les types char et Small du compilateur C sont signés.</span><span class="sxs-lookup"><span data-stu-id="1a72f-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="1a72f-141">Pour correspondre à la valeur par défaut MIDL pour **char**, le compilateur MIDL doit convertir toutes les utilisations de **char** non accompagnées d’une spécification de signe en **char non signé**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="1a72f-142">Le [**petit**](small.md) type n’est pas modifié, car la valeur par défaut de ce compilateur C correspond à la valeur par défaut MIDL pour **Small**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="1a72f-143">L’option non signée **/char** indique que le type de [**caractère**](char-idl.md) du compilateur C n’est pas signé.</span><span class="sxs-lookup"><span data-stu-id="1a72f-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="1a72f-144">Le compilateur MIDL convertit toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe à une **signature** de **petite taille**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="1a72f-145">L’option ascii7 indique qu’aucune spécification de signe explicite n’est ajoutée aux types [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="1a72f-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="1a72f-146">Le type [**petit**](small.md) est généré en tant que **petit**.</span><span class="sxs-lookup"><span data-stu-id="1a72f-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="1a72f-147">Pour éviter toute confusion, vous devez utiliser des spécifications de signe explicite pour les types [**char**](char-idl.md) et Small dans la mesure du possible dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="1a72f-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="1a72f-148">Notez que l’utilisation de types de **caractères** signés de manière explicite dans votre fichier IDL n’est pas prise en charge par l’IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="1a72f-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="1a72f-149">Par conséquent, cette fonctionnalité n’est pas disponible quand vous compilez avec le commutateur MIDL [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="1a72f-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="1a72f-150">Pour plus d’informations sur **/char**, consultez [**petit**](small.md).</span><span class="sxs-lookup"><span data-stu-id="1a72f-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1a72f-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a72f-151">Examples</span></span>

<span data-ttu-id="1a72f-152">**MIDL/char signé nom de fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1a72f-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="1a72f-153">**MIDL/char unsigned filename. idl**</span><span class="sxs-lookup"><span data-stu-id="1a72f-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="1a72f-154">**MIDL/char ascii7 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1a72f-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1a72f-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a72f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a72f-156">**Char**</span><span class="sxs-lookup"><span data-stu-id="1a72f-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="1a72f-157">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1a72f-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1a72f-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="1a72f-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="1a72f-159">**Small**</span><span class="sxs-lookup"><span data-stu-id="1a72f-159">**small**</span></span>](small.md)
</dt> </dl>

 

 




