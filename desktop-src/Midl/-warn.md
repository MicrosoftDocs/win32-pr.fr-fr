---
title: commutateur/WARN
description: Le commutateur/WARN spécifie le niveau d’avertissement du compilateur MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- commutateur/WARN MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678333"
---
# <a name="warn-switch"></a><span data-ttu-id="b10b8-104">commutateur/WARN</span><span class="sxs-lookup"><span data-stu-id="b10b8-104">/warn switch</span></span>

<span data-ttu-id="b10b8-105">Le commutateur **/WARN** spécifie le niveau d’avertissement du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="b10b8-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="b10b8-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="b10b8-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b10b8-107">*level*</span><span class="sxs-lookup"><span data-stu-id="b10b8-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="b10b8-108">Spécifie le niveau d’avertissement, un entier compris entre 0 et 4.</span><span class="sxs-lookup"><span data-stu-id="b10b8-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="b10b8-109">Il n’y a pas d’espace entre le commutateur **/WARN** et le chiffre indiquant la valeur de niveau avertissement.</span><span class="sxs-lookup"><span data-stu-id="b10b8-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b10b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b10b8-110">Remarks</span></span>

<span data-ttu-id="b10b8-111">Le niveau d’avertissement indique la gravité de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="b10b8-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="b10b8-112">Les niveaux d’avertissement sont compris entre 1 et 4, avec une valeur égale à zéro pour ne pas afficher d’informations d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="b10b8-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="b10b8-113">L’avertissement de gravité la plus élevée est le niveau 1.</span><span class="sxs-lookup"><span data-stu-id="b10b8-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="b10b8-114">Le tableau suivant décrit les avertissements pour chaque niveau d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="b10b8-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="b10b8-115">Niveau d’avertissement</span><span class="sxs-lookup"><span data-stu-id="b10b8-115">Warning level</span></span> | <span data-ttu-id="b10b8-116">Description</span><span class="sxs-lookup"><span data-stu-id="b10b8-116">Description</span></span>                                             | <span data-ttu-id="b10b8-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="b10b8-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b10b8-118">0</span><span class="sxs-lookup"><span data-stu-id="b10b8-118">0</span></span>             | <span data-ttu-id="b10b8-119">Aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="b10b8-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="b10b8-120">1</span><span class="sxs-lookup"><span data-stu-id="b10b8-120">1</span></span>             | <span data-ttu-id="b10b8-121">Avertissements sérieux qui peuvent provoquer des erreurs d’application.</span><span class="sxs-lookup"><span data-stu-id="b10b8-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="b10b8-122">Aucun handle de liaison spécifié, pointeurs non attributés, commutateurs en conflit.</span><span class="sxs-lookup"><span data-stu-id="b10b8-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="b10b8-123">2</span><span class="sxs-lookup"><span data-stu-id="b10b8-123">2</span></span>             | <span data-ttu-id="b10b8-124">Peut entraîner des problèmes dans l’environnement d’exploitation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b10b8-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="b10b8-125">La longueur de l’identificateur dépasse 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="b10b8-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="b10b8-126">Aucun ARM d’Union par défaut n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="b10b8-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="b10b8-127">3</span><span class="sxs-lookup"><span data-stu-id="b10b8-127">3</span></span>             | <span data-ttu-id="b10b8-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b10b8-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="b10b8-129">4</span><span class="sxs-lookup"><span data-stu-id="b10b8-129">4</span></span>             | <span data-ttu-id="b10b8-130">Niveau d’avertissement le plus bas.</span><span class="sxs-lookup"><span data-stu-id="b10b8-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="b10b8-131">Constructions non-ANSI C.</span><span class="sxs-lookup"><span data-stu-id="b10b8-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="b10b8-132">Les avertissements sont différents des erreurs.</span><span class="sxs-lookup"><span data-stu-id="b10b8-132">Warnings are different from errors.</span></span> <span data-ttu-id="b10b8-133">Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="b10b8-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="b10b8-134">Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="b10b8-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="b10b8-135">Le niveau d’avertissement défini par le commutateur **/WARN** peut être utilisé avec le commutateur [**WX**](-wx.md) pour faire en sorte que le compilateur MIDL arrête le traitement du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="b10b8-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="b10b8-136">Le commutateur **/WARN** se comporte de la même façon que le commutateur [**/w**](-w.md) .</span><span class="sxs-lookup"><span data-stu-id="b10b8-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="b10b8-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="b10b8-137">Examples</span></span>

<span data-ttu-id="b10b8-138">**MIDL/warn2 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="b10b8-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="b10b8-139">**/warn4. idl de la barre MIDL**</span><span class="sxs-lookup"><span data-stu-id="b10b8-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b10b8-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b10b8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10b8-141">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="b10b8-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




