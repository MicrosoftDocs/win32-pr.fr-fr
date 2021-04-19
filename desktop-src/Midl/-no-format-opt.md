---
title: commutateur/no_format_opt
description: Le commutateur de mise en forme de/non \_ \_ modifie la manière dont MIDL optimise les descripteurs de type et de procédure.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /commutateur no_format_opt MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d6e54b963c9637c4f5a583fc9d8f44a0f2880e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510655"
---
# <a name="no_format_opt-switch"></a><span data-ttu-id="3e802-104">commutateur d’option de mise en forme de/non \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e802-104">/no\_format\_opt switch</span></span>

<span data-ttu-id="3e802-105">Le commutateur de **\_ mise en forme \_ de/non** modifie la manière dont MIDL optimise les descripteurs de type et de procédure.</span><span class="sxs-lookup"><span data-stu-id="3e802-105">The **/no\_format\_opt** switch changes the way MIDL optimizes type and procedure descriptors.</span></span>

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a><span data-ttu-id="3e802-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="3e802-106">Switch Options</span></span>

<span data-ttu-id="3e802-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3e802-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e802-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3e802-108">Remarks</span></span>

<span data-ttu-id="3e802-109">Par défaut, MIDL élimine les descripteurs de type et de procédure en double afin de réduire la taille du code stub généré.</span><span class="sxs-lookup"><span data-stu-id="3e802-109">By default, MIDL eliminates duplicate type and procedure descriptors in order to reduce the size of the generated stub code.</span></span> <span data-ttu-id="3e802-110">L’utilisation du commutateur **\_ \_ OPT au format/non** désactive ce comportement d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="3e802-110">Using the **/no\_format\_opt** switch turns off this optimizing behavior.</span></span>

## <a name="examples"></a><span data-ttu-id="3e802-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e802-111">Examples</span></span>

<span data-ttu-id="3e802-112">**format MIDL \_ /non \_ OPT mylean. idl**</span><span class="sxs-lookup"><span data-stu-id="3e802-112">**midl /no\_format\_opt mylean.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3e802-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e802-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e802-114">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="3e802-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3e802-115">**/OI**</span><span class="sxs-lookup"><span data-stu-id="3e802-115">**/Oi**</span></span>](-oi.md)
</dt> </dl>

 

 




