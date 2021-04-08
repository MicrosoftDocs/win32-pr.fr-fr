---
title: commutateur/cpp_cmd
description: Le \_ commutateur/CPP cmd spécifie le préprocesseur que le compilateur MIDL utilise pour prétraiter les fichiers d’entrée.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /commutateur cpp_cmd MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678665"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="5fed3-104">\_commutateur cmd/CPP</span><span class="sxs-lookup"><span data-stu-id="5fed3-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="5fed3-105">Le commutateur **/CPP \_ cmd** spécifie le préprocesseur que le compilateur MIDL utilise pour prétraiter les fichiers d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5fed3-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="5fed3-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5fed3-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="5fed3-107">*\_Binaire de préprocesseur \_ C*</span><span class="sxs-lookup"><span data-stu-id="5fed3-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="5fed3-108">Spécifie la commande qui appelle le préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="5fed3-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="5fed3-109">Cette commande permet aux développeurs de remplacer le préprocesseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fed3-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="5fed3-110">Par défaut, MIDL appelle le compilateur Microsoft C/C++ à partir de l’environnement de génération de l’ordinateur de Build.</span><span class="sxs-lookup"><span data-stu-id="5fed3-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fed3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5fed3-111">Remarks</span></span>

<span data-ttu-id="5fed3-112">L' *argument \_ \_ binaire du préprocesseur C* du commutateur peut spécifier le chemin d’accès complet ; le suffixe et les guillemets de l’exe sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5fed3-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="5fed3-113">En règle générale, les développeurs utilisent le commutateur pour choisir une version particulière du préprocesseur Microsoft C/C++ ou équivalent dans l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="5fed3-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="5fed3-114">Dans ce cas, il n’est pas nécessaire d’utiliser le commutateur [**/CPP \_ OPT**](-cpp-opt.md) avec **/CPP \_ cmd**.</span><span class="sxs-lookup"><span data-stu-id="5fed3-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="5fed3-115">Lors de l’utilisation d’un préprocesseur non-Microsoft, en particulier lorsque le préprocesseur spécifié ne dirige pas sa sortie vers stdout, le commutateur du compilateur C qui redirige la sortie vers stdout dans le cadre du commutateur [**/CPP \_ OPT**](-cpp-opt.md) du compilateur MIDL doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="5fed3-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="5fed3-116">Pour plus d’informations [, consultez Configuration requise pour le préprocesseur C pour MIDL](c-preprocessor-requirements-for-midl.md)</span><span class="sxs-lookup"><span data-stu-id="5fed3-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="5fed3-117">Le préprocesseur est appelé par une chaîne de commande qui est formée à partir des informations fournies au compilateur MIDL par **/CPP \_ cmd**, [**/CPP \_ OPT**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)et [**/u**](-u.md) commutateurs.</span><span class="sxs-lookup"><span data-stu-id="5fed3-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="5fed3-118">Le tableau suivant résume la construction de la chaîne de commande pour chaque combinaison de commutateurs **/CPP \_ cmd** et **/CPP \_ OPT** .</span><span class="sxs-lookup"><span data-stu-id="5fed3-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="5fed3-119">Lorsque le commutateur **/CPP \_ cmd** n’est pas spécifié, le compilateur MIDL appelle le compilateur Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="5fed3-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="5fed3-120">MIDL utilise un binaire Cl.exe trouvé dans l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="5fed3-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="5fed3-121">Quand le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas présent, le compilateur MIDL concatène la chaîne spécifiée par le **commutateur \_ /CPP cmd** avec les informations spécifiées par les options MIDL [**/i**](-i.md), [**/d**](-d.md) et [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="5fed3-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="5fed3-122">La chaîne/E est également concaténée à la chaîne d’appel du compilateur C pour indiquer que le compilateur C/C++ doit effectuer un prétraitement uniquement.</span><span class="sxs-lookup"><span data-stu-id="5fed3-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="5fed3-123">Le commutateur [**/nologo**](-nologo.md) est ajouté pour supprimer la bannière du compilateur C/C++.</span><span class="sxs-lookup"><span data-stu-id="5fed3-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="5fed3-124">Le compilateur MIDL utilise la chaîne concaténée pour appeler le préprocesseur C pour le fichier IDL de niveau supérieur, ainsi que pour les fichiers IDL importés, ainsi que pour tous les fichiers ACF existants.</span><span class="sxs-lookup"><span data-stu-id="5fed3-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="5fed3-125">Quand le commutateur [**/CPP \_ OPT**](-cpp-opt.md) est présent, ce qui doit être un cas rare pour les plateformes actuelles 32 bits et 64 bits, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec la chaîne spécifiée par le commutateur d’activation **/CPP \_** .</span><span class="sxs-lookup"><span data-stu-id="5fed3-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="5fed3-126">Le compilateur MIDL utilise la chaîne concaténée pour appeler le binaire de préprocesseur indiqué à la place du préprocesseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fed3-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="5fed3-127">Lorsque le **commutateur/CPP \_ OPT** est présent, ni les options du compilateur MIDL spécifiées par les commutateurs [**/I**](-i.md), [**/d**](-d.md)et [**/U**](-u.md) , ni le commutateur/e du compilateur C ne sont concaténées avec la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5fed3-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="5fed3-128">Vous devez fournir l’option/E, ou équivalent, dans le cadre de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5fed3-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="5fed3-129">/CPP \_ cmd est présent ?</span><span class="sxs-lookup"><span data-stu-id="5fed3-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="5fed3-130">/CPP \_ OPT est présent ?</span><span class="sxs-lookup"><span data-stu-id="5fed3-130">/cpp\_opt present?</span></span> | <span data-ttu-id="5fed3-131">Description</span><span class="sxs-lookup"><span data-stu-id="5fed3-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fed3-132">Non (par défaut)</span><span class="sxs-lookup"><span data-stu-id="5fed3-132">No (default)</span></span>       | <span data-ttu-id="5fed3-133">Non (par défaut)</span><span class="sxs-lookup"><span data-stu-id="5fed3-133">No (default)</span></span>       | <span data-ttu-id="5fed3-134">Appelle le compilateur Microsoft C/C++ par défaut avec les paramètres obtenus à partir des commutateurs MIDL [**/i**](-i.md), [**/d**](-d.md) et [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="5fed3-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="5fed3-135">Ajoute les commutateurs de préprocesseur/E et [**/nologo**](-nologo.md).</span><span class="sxs-lookup"><span data-stu-id="5fed3-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="5fed3-136">Oui</span><span class="sxs-lookup"><span data-stu-id="5fed3-136">Yes</span></span>                | <span data-ttu-id="5fed3-137">Non</span><span class="sxs-lookup"><span data-stu-id="5fed3-137">No</span></span>                 | <span data-ttu-id="5fed3-138">Appelle le binaire de préprocesseur indiqué avec les mêmes commutateurs que ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5fed3-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="5fed3-139">Non</span><span class="sxs-lookup"><span data-stu-id="5fed3-139">No</span></span>                 | <span data-ttu-id="5fed3-140">Oui</span><span class="sxs-lookup"><span data-stu-id="5fed3-140">Yes</span></span>                | <span data-ttu-id="5fed3-141">Appelle le compilateur Microsoft C avec les options spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5fed3-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="5fed3-142">N’utilise pas les options MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="5fed3-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="5fed3-143">Vous devez fournir/E dans le cadre de l’option [**/CPP \_ OPT**](-cpp-opt.md).</span><span class="sxs-lookup"><span data-stu-id="5fed3-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="5fed3-144">Oui</span><span class="sxs-lookup"><span data-stu-id="5fed3-144">Yes</span></span>                | <span data-ttu-id="5fed3-145">Oui</span><span class="sxs-lookup"><span data-stu-id="5fed3-145">Yes</span></span>                | <span data-ttu-id="5fed3-146">Appelle le binaire de préprocesseur spécifié avec les options spécifiées uniquement.</span><span class="sxs-lookup"><span data-stu-id="5fed3-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="5fed3-147">Vous devez utiliser des guillemets.</span><span class="sxs-lookup"><span data-stu-id="5fed3-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="5fed3-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="5fed3-148">Examples</span></span>

<span data-ttu-id="5fed3-149">**MIDL/CPP \_ cmd d : \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC : \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="5fed3-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="5fed3-150">**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC : \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="5fed3-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="5fed3-151">**MIDL/CPP \_ OPT "/E/DFLAG = true/IC : \\ Inc" nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5fed3-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="5fed3-152">**MIDL/CPP \_ cmd "cl"/CPP \_ OPT "/e/DFLAG = true/IC : \\ Inc" nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5fed3-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5fed3-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fed3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fed3-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="5fed3-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="5fed3-155">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="5fed3-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="5fed3-156">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="5fed3-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5fed3-157">**/non \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="5fed3-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="5fed3-158">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="5fed3-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




