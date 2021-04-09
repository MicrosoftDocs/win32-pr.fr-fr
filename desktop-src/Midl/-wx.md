---
title: /WX (commutateur)
description: Le commutateur/WX demande au compilateur MIDL de gérer toutes les erreurs au niveau d’avertissement donné comme des erreurs.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX, commutateur MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841386"
---
# <a name="wx-switch"></a><span data-ttu-id="94762-104">/WX (commutateur)</span><span class="sxs-lookup"><span data-stu-id="94762-104">/WX switch</span></span>

<span data-ttu-id="94762-105">Le commutateur **/WX** demande au compilateur MIDL de gérer toutes les erreurs au niveau d’avertissement donné comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="94762-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="94762-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="94762-106">Switch Options</span></span>

<span data-ttu-id="94762-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="94762-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="94762-108">Notes</span><span class="sxs-lookup"><span data-stu-id="94762-108">Remarks</span></span>

<span data-ttu-id="94762-109">Si le commutateur **/WX** est spécifié et que le commutateur [**/w**](-w.md)*n* n’est pas spécifié, tous les avertissements au niveau par défaut, Level 1, sont traités comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="94762-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="94762-110">Le commutateur [**/w**](-w.md)*n* indique au compilateur d’afficher tous les avertissements au niveau *n* et **/WX** indique au compilateur de gérer tous les avertissements comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="94762-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="94762-111">La combinaison de ces deux commutateurs indique au compilateur de gérer tous les avertissements au niveau *n* comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="94762-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="94762-112">Les erreurs sont différentes des avertissements.</span><span class="sxs-lookup"><span data-stu-id="94762-112">Errors are different from warnings.</span></span> <span data-ttu-id="94762-113">Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="94762-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="94762-114">Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="94762-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="94762-115">AVERTISSEMENT : le niveau zéro (0) indique au compilateur MIDL de supprimer les informations d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="94762-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="94762-116">Lorsque les commutateurs **/W0** et **/WX** sont combinés, le compilateur MIDL supprime toutes les informations d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="94762-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="94762-117">Dans ce cas, le commutateur **/WX** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="94762-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="94762-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="94762-118">Examples</span></span>

<span data-ttu-id="94762-119">**MIDL/WX nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="94762-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="94762-120">**MIDL/W3/WX nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="94762-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="94762-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94762-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94762-122">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="94762-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="94762-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="94762-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




