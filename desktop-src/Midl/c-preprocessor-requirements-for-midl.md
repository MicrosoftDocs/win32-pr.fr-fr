---
title: C-Configuration requise pour le préprocesseur pour MIDL
description: Cette page s’applique uniquement aux développeurs qui ont des raisons spécifiques de remplacer le préprocesseur Microsoft C/C++ comme préprocesseur utilisé par MIDL, ou aux développeurs qui doivent spécifier des commutateurs de préprocesseur personnalisés.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL du compilateur MIDL, C-preprocesseur, configuration requise
- C-preprocesseur MIDL, configuration requise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940191"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="61c8f-105">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="61c8f-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="61c8f-106">Cette page s’applique uniquement aux développeurs qui ont des raisons spécifiques de remplacer le préprocesseur Microsoft C/C++ comme préprocesseur utilisé par MIDL, ou aux développeurs qui doivent spécifier des commutateurs de préprocesseur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="61c8f-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="61c8f-107">Les commutateurs MIDL [**/CPP \_ cmd**](-cpp-cmd.md), [**/CPP \_ OPT**](-cpp-opt.md)et [**/non \_ CPP**](-no-cpp-nocpp.md) sont utilisés pour remplacer le comportement par défaut du compilateur.</span><span class="sxs-lookup"><span data-stu-id="61c8f-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="61c8f-108">Il n’y a généralement aucune raison de remplacer le préprocesseur Microsoft C/C++, ni de spécifier des commutateurs de préprocesseur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="61c8f-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="61c8f-109">Le compilateur MIDL utilise un préprocesseur C lors du traitement initial du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="61c8f-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="61c8f-110">L’environnement de génération utilisé lors de la compilation des fichiers IDL est associé à un préprocesseur C/C++ par défaut.</span><span class="sxs-lookup"><span data-stu-id="61c8f-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="61c8f-111">Si un autre préprocesseur doit être utilisé, le commutateur de compilateur MIDL [**/CPP \_ cmd**](-cpp-cmd.md) active une substitution du nom de préprocesseur C/C++ par défaut :</span><span class="sxs-lookup"><span data-stu-id="61c8f-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="61c8f-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nom du préprocesseur \_*</span><span class="sxs-lookup"><span data-stu-id="61c8f-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="61c8f-113">Spécifie le nom du préprocesseur à utiliser par MIDL.</span><span class="sxs-lookup"><span data-stu-id="61c8f-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="61c8f-114">Peut être spécifié avec un chemin d’accès au fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="61c8f-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="61c8f-115">L’extension. exe est facultative.</span><span class="sxs-lookup"><span data-stu-id="61c8f-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="61c8f-116"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="61c8f-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="61c8f-117">Spécifie le nom du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="61c8f-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="61c8f-118">Le compilateur MIDL s’attend à ce que le préprocesseur respecte les conventions suivantes :</span><span class="sxs-lookup"><span data-stu-id="61c8f-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="61c8f-119">Le fichier d’entrée est spécifié en tant que dernier argument sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="61c8f-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="61c8f-120">Le préprocesseur doit rediriger la sortie vers le périphérique de sortie standard, stdout.</span><span class="sxs-lookup"><span data-stu-id="61c8f-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="61c8f-121">Dans le flux de sortie du préprocesseur, les directives de **\# ligne** sont présentes pour permettre de meilleurs messages de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="61c8f-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="61c8f-122">Les directives de ligne sont les seules directives de préprocesseur dans le flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="61c8f-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="61c8f-123">MIDL part du principe que le préprocesseur généré a supprimé toutes les directives de préprocesseur du flux d’entrée du compilateur, à l’exception des occurrences de la directive de ligne nécessaire pour identifier l’emplacement source dans les messages du compilateur.</span><span class="sxs-lookup"><span data-stu-id="61c8f-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="61c8f-124">Lorsque vous indiquez un préprocesseur différent du préprocesseur Microsoft C/C++, ou lorsque vous spécifiez des options de préprocesseur avec le commutateur [**/CPP \_ OPT**](-cpp-opt.md) , la spécification d’une option de préprocesseur appropriée qui place les directives de ligne dans le flux d’entrée du compilateur est requise.</span><span class="sxs-lookup"><span data-stu-id="61c8f-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="61c8f-125">Par exemple, pour le préprocesseur Microsoft C/C++, l’option **/e** devrait être utilisée :</span><span class="sxs-lookup"><span data-stu-id="61c8f-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="61c8f-126">La directive de **\# ligne** est acceptée par MIDL sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="61c8f-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="61c8f-127">Pour obtenir une description complète de la directive de ligne et des autres directives de préprocesseur, consultez la documentation du compilateur C utilisé.</span><span class="sxs-lookup"><span data-stu-id="61c8f-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="61c8f-128">MIDL accepte uniquement la directive de préprocesseur de ligne.</span><span class="sxs-lookup"><span data-stu-id="61c8f-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="61c8f-129">Par conséquent, si le commutateur [**/non \_ CPP**](-no-cpp-nocpp.md) est utilisé, le fichier d’entrée ne doit pas avoir d’autres directives de préprocesseur ou le fichier d’entrée doit avoir été traité avant l’appel de MIDL.</span><span class="sxs-lookup"><span data-stu-id="61c8f-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="61c8f-130">Pour plus d’informations, consultez [gestion des \# définitions dans les fichiers IDL](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="61c8f-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




