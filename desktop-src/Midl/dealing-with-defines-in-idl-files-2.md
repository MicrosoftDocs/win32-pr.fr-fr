---
title: Gestion des définitions dans les fichiers IDL
description: Cette page décrit les raisons pour lesquelles les symboles définis avec une \ define disparaissent des fichiers H générés par le compilateur MIDL et ce que vous pouvez en faire. Cette explication s’applique à tous les fichiers traités par MIDL, tels que les fichiers \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL du compilateur MIDL, traitant des définitions
- définit MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029166"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="c05a3-106">Gestion des \# définitions dans les fichiers IDL</span><span class="sxs-lookup"><span data-stu-id="c05a3-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="c05a3-107">Cette page décrit les raisons pour lesquelles les symboles définis avec une **\# définition** disparaissent des fichiers H générés par le compilateur MIDL et ce que vous pouvez en faire.</span><span class="sxs-lookup"><span data-stu-id="c05a3-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="c05a3-108">Cette explication s’applique à tous les fichiers traités par MIDL, tels que les \* fichiers. idl, \* . ACF et \* . h.</span><span class="sxs-lookup"><span data-stu-id="c05a3-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="c05a3-109">La disparition des symboles de **\# définition** est le résultat de la délégation par MIDL du prétraitement des fichiers d’entrée à un préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="c05a3-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="c05a3-110">Par défaut, le préprocesseur est un préprocesseur C/C++ de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="c05a3-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="c05a3-111">Après le prétraitement, le processus MIDL de flux d’entrée reçoit uniquement des \# directives de préprocesseur de ligne.</span><span class="sxs-lookup"><span data-stu-id="c05a3-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="c05a3-112">En particulier, le préprocesseur déroulera toutes les définitions de macros dans les fichiers d’entrée, et par conséquent, MIDL ne peut pas détecter sa présence.</span><span class="sxs-lookup"><span data-stu-id="c05a3-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="c05a3-113">Par conséquent, lorsque MIDL réplique les définitions de types à partir d’un fichier d’entrée dans le fichier H généré, les définitions ne \# sont pas répliquées.</span><span class="sxs-lookup"><span data-stu-id="c05a3-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="c05a3-114">Par conséquent, n’utilisez pas \# de définit directement dans les fichiers IDL s’ils doivent être utilisés ultérieurement à partir du fichier H généré.</span><span class="sxs-lookup"><span data-stu-id="c05a3-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="c05a3-115">Les quatre solutions de contournement suivantes sont recommandées :</span><span class="sxs-lookup"><span data-stu-id="c05a3-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="c05a3-116">Utilisez la spécification de Déclaration [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="c05a3-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="c05a3-117">Utilisez des fichiers d’en-tête distincts qui sont importés ou inclus dans le fichier IDL, puis inclus ultérieurement dans le code source C.</span><span class="sxs-lookup"><span data-stu-id="c05a3-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="c05a3-118">Utilisez des constantes d’énumération dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="c05a3-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="c05a3-119">Utilisez [**le \_ Devis RPC**](cpp-quote.md) pour reproduire la **\# définition** dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="c05a3-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="c05a3-120">Vous pouvez reproduire des constantes de manifeste à l’aide de la **syntaxe de déclaration de constante IDL**.</span><span class="sxs-lookup"><span data-stu-id="c05a3-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="c05a3-121">Notez que le [**const**](const.md) dans la déclaration de constante IDL est différent de la sémantique **const** C/C++ et introduit simplement une constante nommée pour une compilation IDL.</span><span class="sxs-lookup"><span data-stu-id="c05a3-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="c05a3-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c05a3-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="c05a3-123">Cet exemple spécifie que **ARRSIZE** est une constante avec une valeur de 10.</span><span class="sxs-lookup"><span data-stu-id="c05a3-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="c05a3-124">Les constantes nommées peuvent être utilisées dans les déclarateurs de tableau IDL et dans d’autres emplacements où un programmeur C utiliserait un manifeste défini.</span><span class="sxs-lookup"><span data-stu-id="c05a3-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="c05a3-125">En outre, cette syntaxe entraîne la génération de la ligne suivante dans le fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c05a3-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="c05a3-126">Une autre façon de gérer **\#** les instructions de définition consiste à les empaqueter dans un fichier d’en-tête distinct, soit dans un fichier dédié pour **\#** définir des instructions, soit dans un fichier qui contient uniquement des définitions de type.</span><span class="sxs-lookup"><span data-stu-id="c05a3-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="c05a3-127">Un fichier qui contient uniquement des directives de préprocesseur peut être inclus en toute sécurité à la fois par le fichier IDL et les fichiers sources C.</span><span class="sxs-lookup"><span data-stu-id="c05a3-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="c05a3-128">Bien que les directives ne soient pas disponibles dans le fichier d’en-tête généré par le compilateur MIDL, le programme source C peut inclure le fichier d’en-tête distinct.</span><span class="sxs-lookup"><span data-stu-id="c05a3-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="c05a3-129">De la même façon, un fichier d’en-tête avec des **\#** instructions de définition et des définitions de type standard peut être importé à partir de votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="c05a3-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="c05a3-130">Cette approche encapsule les **\#** instructions define et typedef en les utilisant dans un fichier H, de sorte que les **\#** symboles de définition ne sont pas utilisés directement dans le fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="c05a3-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="c05a3-131">L’importation d’un fichier d’en-tête ou d’un fichier IDL dans un autre fichier IDL empêche les instructions typedef d’être répliquées dans le fichier H généré par MIDL (contrairement aux **\#** instructions Include).</span><span class="sxs-lookup"><span data-stu-id="c05a3-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="c05a3-132">Cette approche permet au fichier d’en-tête d’origine d’être référencé en toute sécurité à partir du code C le long du fichier H généré sans avoir de problème avec les définitions dupliquées.</span><span class="sxs-lookup"><span data-stu-id="c05a3-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="c05a3-133">L’utilisation de constantes d’énumération dans le fichier IDL est également effective.</span><span class="sxs-lookup"><span data-stu-id="c05a3-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="c05a3-134">Ces constantes peuvent être utilisées dans des expressions constantes dans IDL, par exemple dans des déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="c05a3-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="c05a3-135">Les constantes d’énumération ne sont pas supprimées lors des premières phases de la compilation MIDL par le préprocesseur du compilateur C. ainsi, les constantes d’énumération sont disponibles dans le fichier d’en-tête généré par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="c05a3-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="c05a3-136">Prenons l'instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="c05a3-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="c05a3-137">Cette instruction ne sera pas supprimée pendant la compilation MIDL par le préprocesseur C et le typedef sera répliqué dans le fichier H généré.</span><span class="sxs-lookup"><span data-stu-id="c05a3-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="c05a3-138">La constante MAXSTRINGCOUNT est disponible pour les programmes source C qui incluent le fichier d’en-tête généré par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="c05a3-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="c05a3-139">Enfin, la directive de [**\_ citation CPP**](cpp-quote.md) de MIDL peut être utilisée pour écrire une chaîne arbitraire directement dans le fichier H généré.</span><span class="sxs-lookup"><span data-stu-id="c05a3-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="c05a3-140">Par exemple, pour obtenir la constante de manifeste utilisée précédemment sur cette page avec le **\_ guillemet CPP**, vous pouvez utiliser l’instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="c05a3-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="c05a3-141">Cette instruction entraîne la génération de la ligne suivante dans le fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c05a3-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 




