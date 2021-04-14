---
title: commutateur/cpp_opt
description: Le \_ commutateur/CPP opt spécifie les options à transmettre au préprocesseur C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /commutateur cpp_opt MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383404"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="c1b7b-104">\_commutateur/CPP opt</span><span class="sxs-lookup"><span data-stu-id="c1b7b-104">/cpp\_opt switch</span></span>

<span data-ttu-id="c1b7b-105">Le commutateur **/CPP \_ OPT** spécifie les options à transmettre au préprocesseur C/C++.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="c1b7b-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="c1b7b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c1b7b-107">*\_Option de préprocesseur \_ C*</span><span class="sxs-lookup"><span data-stu-id="c1b7b-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="c1b7b-108">Spécifie l’option de ligne de commande associée au préprocesseur appelé.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="c1b7b-109">**Remarque**: pour les préprocesseurs Microsoft C/C++, vous devez fournir le `/E` commutateur dans le cadre de la chaîne d' *\_ \_ option de préprocesseur c* .</span><span class="sxs-lookup"><span data-stu-id="c1b7b-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="c1b7b-110">Des guillemets sont requis lorsque plusieurs options sont utilisées, et pour les espaces.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b7b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c1b7b-111">Remarks</span></span>

<span data-ttu-id="c1b7b-112">N’utilisez pas ce commutateur à moins qu’il y ait une raison spécifique.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="c1b7b-113">Pour obtenir des informations importantes sur le prétraitement, consultez la [Configuration requise pour le préprocesseur C pour MIDL](c-preprocessor-requirements-for-midl.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b7b-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="c1b7b-114">Le commutateur **/CPP \_ OPT** peut être utilisé avec ou sans le commutateur [**/CPP \_ cmd**](-cpp-cmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b7b-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="c1b7b-115">Consultez **/CPP \_ cmd** pour plus d’informations sur la construction de la ligne de commande du préprocesseur dans les deux cas.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="c1b7b-116">Le commutateur **/CPP \_ OPT** , s’il est spécifié, doit toujours être inclus `/E` pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="c1b7b-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="c1b7b-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c1b7b-117">Examples</span></span>

<span data-ttu-id="c1b7b-118">**MIDL/CPP \_ cmd d : \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC : \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c1b7b-119">**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC : \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c1b7b-120">**MIDL/CPP \_ OPT "/E/DFLAG = true/IC : \\ Inc" nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="c1b7b-121">**MIDL/CPP \_ cmd "cl"/CPP \_ OPT "/e/DFLAG = true/IC : \\ Inc" nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c1b7b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b7b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b7b-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="c1b7b-124">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="c1b7b-125">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="c1b7b-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c1b7b-126">**/non \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="c1b7b-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="c1b7b-127">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="c1b7b-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




