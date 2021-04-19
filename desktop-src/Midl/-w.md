---
title: Bouton/w
description: Le commutateur/W spécifie le niveau d’avertissement du compilateur MIDL. Le niveau d’avertissement indique la gravité de l’avertissement.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W, commutateur MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511657"
---
# <a name="w-switch"></a><span data-ttu-id="19c26-105">Bouton/w</span><span class="sxs-lookup"><span data-stu-id="19c26-105">/W switch</span></span>

<span data-ttu-id="19c26-106">Le commutateur **/w** spécifie le niveau d’avertissement du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="19c26-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="19c26-107">Le niveau d’avertissement indique la gravité de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="19c26-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="19c26-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="19c26-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="19c26-109">*level*</span><span class="sxs-lookup"><span data-stu-id="19c26-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="19c26-110">Spécifie le niveau d’avertissement, un entier compris entre 0 et 4.</span><span class="sxs-lookup"><span data-stu-id="19c26-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="19c26-111">Il n’y a pas d’espace entre le commutateur **/w** et le chiffre indiquant la valeur de niveau avertissement.</span><span class="sxs-lookup"><span data-stu-id="19c26-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19c26-112">Notes</span><span class="sxs-lookup"><span data-stu-id="19c26-112">Remarks</span></span>

<span data-ttu-id="19c26-113">Les niveaux d’avertissement sont compris entre 1 et 4, avec une valeur égale à zéro pour ne pas afficher d’informations d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="19c26-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="19c26-114">L’avertissement de gravité la plus élevée est de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="19c26-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="19c26-115">Le tableau suivant décrit les avertissements pour chaque niveau d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="19c26-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="19c26-116">Niveau d’avertissement</span><span class="sxs-lookup"><span data-stu-id="19c26-116">Warning level</span></span> | <span data-ttu-id="19c26-117">Description</span><span class="sxs-lookup"><span data-stu-id="19c26-117">Description</span></span>                                             | <span data-ttu-id="19c26-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="19c26-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="19c26-119">W0</span><span class="sxs-lookup"><span data-stu-id="19c26-119">W0</span></span>            | <span data-ttu-id="19c26-120">Aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="19c26-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="19c26-121">W1</span><span class="sxs-lookup"><span data-stu-id="19c26-121">W1</span></span>            | <span data-ttu-id="19c26-122">Avertissements sérieux qui peuvent provoquer des erreurs d’application.</span><span class="sxs-lookup"><span data-stu-id="19c26-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="19c26-123">Aucun handle de liaison spécifié, pointeurs non attributés, commutateurs en conflit.</span><span class="sxs-lookup"><span data-stu-id="19c26-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="19c26-124">W2</span><span class="sxs-lookup"><span data-stu-id="19c26-124">W2</span></span>            | <span data-ttu-id="19c26-125">Peut entraîner des problèmes dans l’environnement d’exploitation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19c26-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="19c26-126">La longueur de l’identificateur dépasse 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="19c26-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="19c26-127">Aucun ARM d’Union par défaut n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="19c26-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="19c26-128">W3</span><span class="sxs-lookup"><span data-stu-id="19c26-128">W3</span></span>            | <span data-ttu-id="19c26-129">Réservé.</span><span class="sxs-lookup"><span data-stu-id="19c26-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="19c26-130">W4</span><span class="sxs-lookup"><span data-stu-id="19c26-130">W4</span></span>            | <span data-ttu-id="19c26-131">Niveau d’avertissement le plus bas.</span><span class="sxs-lookup"><span data-stu-id="19c26-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="19c26-132">Constructions non-ANSI C.</span><span class="sxs-lookup"><span data-stu-id="19c26-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="19c26-133">Les avertissements sont différents des erreurs.</span><span class="sxs-lookup"><span data-stu-id="19c26-133">Warnings are different from errors.</span></span> <span data-ttu-id="19c26-134">Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="19c26-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="19c26-135">Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="19c26-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="19c26-136">Le niveau d’avertissement défini par le commutateur **/w** peut être utilisé avec le commutateur [**/WX**](-wx.md) pour faire en sorte que le compilateur MIDL arrête le traitement du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="19c26-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="19c26-137">Le commutateur **/w** se comporte de la même façon que le commutateur [**/WARN**](-warn.md) .</span><span class="sxs-lookup"><span data-stu-id="19c26-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="19c26-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="19c26-138">Examples</span></span>

<span data-ttu-id="19c26-139">**MIDL/W2 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="19c26-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="19c26-140">**/W4. idl de la barre MIDL**</span><span class="sxs-lookup"><span data-stu-id="19c26-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="19c26-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19c26-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c26-142">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="19c26-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="19c26-143">**/WARN**</span><span class="sxs-lookup"><span data-stu-id="19c26-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




