---
title: commutateur/no_robust
description: Le commutateur de la \_ robustesse de/non indique au compilateur MIDL de désactiver explicitement la fonctionnalité de ligne de commande/Robust. Le commutateur de ligne de commande/Robust et les fonctionnalités qui lui sont associées sont le paramètre de compilateur par défaut pour MIDL version 6.0.359 et versions ultérieures.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /commutateur no_robust MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678714"
---
# <a name="no_robust-switch"></a><span data-ttu-id="50692-105">\_Sélecteur de commutateur robuste</span><span class="sxs-lookup"><span data-stu-id="50692-105">/no\_robust switch</span></span>

<span data-ttu-id="50692-106">Le commutateur de la **\_ robustesse de/non** indique au compilateur MIDL de désactiver explicitement la fonctionnalité de ligne de commande [**/Robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="50692-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="50692-107">Le commutateur de ligne de commande **/Robust** et les fonctionnalités qui lui sont associées sont le paramètre de compilateur par défaut pour MIDL version 6.0.359 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="50692-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="50692-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="50692-108">Switch Options</span></span>

<span data-ttu-id="50692-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="50692-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="50692-110">Notes</span><span class="sxs-lookup"><span data-stu-id="50692-110">Remarks</span></span>

<span data-ttu-id="50692-111">Avec MIDL version 6.0.359 et ultérieure, le compilateur MIDL définit [**/Robust**](-robust.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="50692-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="50692-112">Le commutateur de ligne de commande **\_ fiable/non** doit être utilisé pour désactiver la fonctionnalité **/Robust** si des stubs générés doivent s’exécuter sur Microsoft WindowsÂ NT, WindowsÂ 95/98 ou sur WindowsÂ me.</span><span class="sxs-lookup"><span data-stu-id="50692-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="50692-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="50692-113">Examples</span></span>

<span data-ttu-id="50692-114">**MIDL \_ . idl de nom de fichier fiable**</span><span class="sxs-lookup"><span data-stu-id="50692-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="50692-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50692-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50692-116">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="50692-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="50692-117">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="50692-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




