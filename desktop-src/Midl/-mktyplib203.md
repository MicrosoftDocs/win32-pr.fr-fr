---
title: commutateur/mktyplib203
description: Le commutateur/mktyplib203 force le compilateur MIDL à analyser le fichier d’entrée.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- MIDL du commutateur/mktyplib203
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841434"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="5f248-104">commutateur/mktyplib203</span><span class="sxs-lookup"><span data-stu-id="5f248-104">/mktyplib203 switch</span></span>

<span data-ttu-id="5f248-105">Le commutateur **/mktyplib203** force le compilateur MIDL à analyser le fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5f248-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="5f248-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5f248-106">Switch Options</span></span>

<span data-ttu-id="5f248-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f248-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f248-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5f248-108">Remarks</span></span>

<span data-ttu-id="5f248-109">Pour pouvoir utiliser le commutateur **/mktyplib203** , le fichier d’entrée doit respecter la syntaxe ODL exactement, ce qui signifie que vous ne pouvez pas placer d’instructions en dehors du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="5f248-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="5f248-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="5f248-110">Examples</span></span>

<span data-ttu-id="5f248-111">**MIDL/mktyplib203 myoldodl. ODL**</span><span class="sxs-lookup"><span data-stu-id="5f248-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="5f248-112">**MIDL/mktyplib203 oldhabit. idl**</span><span class="sxs-lookup"><span data-stu-id="5f248-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5f248-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f248-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f248-114">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="5f248-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5f248-115">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="5f248-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




