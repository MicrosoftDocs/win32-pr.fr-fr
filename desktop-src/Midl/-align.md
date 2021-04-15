---
title: commutateur/align
description: Le commutateur/align est fonctionnellement identique à l’option/ZP/ZP et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- MIDL du commutateur/align
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507614"
---
# <a name="align-switch"></a><span data-ttu-id="98033-104">commutateur/align</span><span class="sxs-lookup"><span data-stu-id="98033-104">/align switch</span></span>

<span data-ttu-id="98033-105">Le commutateur **/align** est fonctionnellement identique à l’option [**/ZP/ZP**](-zp.md) et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec mktyplib.</span><span class="sxs-lookup"><span data-stu-id="98033-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="98033-106">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="98033-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="98033-107">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="98033-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="98033-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="98033-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="98033-109">*repère*</span><span class="sxs-lookup"><span data-stu-id="98033-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="98033-110">Spécifie l’alignement pour les types dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="98033-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="98033-111">La valeur d' *alignement* peut être 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="98033-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="98033-112">La valeur 1 indique l’alignement naturel ; *n* indique l’alignement sur l’octet *n*.</span><span class="sxs-lookup"><span data-stu-id="98033-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="98033-113">Si vous ne spécifiez pas le commutateur **/align** , la valeur par défaut est 8.</span><span class="sxs-lookup"><span data-stu-id="98033-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98033-114">Notes</span><span class="sxs-lookup"><span data-stu-id="98033-114">Remarks</span></span>

<span data-ttu-id="98033-115">Si vous générez un nouveau Makefile, utilisez le commutateur [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="98033-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="98033-116">La valeur d’alignement correspond à la valeur de l’option [**/ZP**](-zp.md) utilisée par le compilateur Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="98033-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="98033-117">Veillez à spécifier le même alignement lorsque vous appelez le compilateur C comme lorsque vous appelez le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="98033-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="98033-118">Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="98033-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="98033-119">Pour plus d’informations sur les risques potentiels liés à l’utilisation de niveaux de compression non standard, consultez la rubrique d’aide [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="98033-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="98033-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="98033-120">Examples</span></span>

<span data-ttu-id="98033-121">**MIDL/align : 4 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="98033-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="98033-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98033-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98033-123">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="98033-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="98033-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="98033-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




