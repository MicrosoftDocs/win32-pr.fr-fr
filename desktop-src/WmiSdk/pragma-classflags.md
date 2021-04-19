---
description: Contrôle la manière dont WMI crée ou met à jour des classes en fonction des indicateurs spécifiés.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536129"
---
# <a name="pragma-classflags"></a><span data-ttu-id="f6f1c-103">pragma classflags</span><span class="sxs-lookup"><span data-stu-id="f6f1c-103">pragma classflags</span></span>

<span data-ttu-id="f6f1c-104">La commande de préprocesseur **pragma classflags** contrôle la manière dont WMI crée ou met à jour des classes en fonction des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="f6f1c-105">La syntaxe de cette commande est décrite ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f6f1c-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="f6f1c-106">L' *\[ indicateur \]* doit être un ou plusieurs des arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="f6f1c-107">Vous pouvez combiner tous les indicateurs qui ne sont pas contradictoires.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="f6f1c-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="f6f1c-108">Flag</span></span>        | <span data-ttu-id="f6f1c-109">Description</span><span class="sxs-lookup"><span data-stu-id="f6f1c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f1c-110">CreateOnly</span><span class="sxs-lookup"><span data-stu-id="f6f1c-110">createonly</span></span>  | <span data-ttu-id="f6f1c-111">Indique au compilateur de ne pas apporter de modifications aux classes existantes et met fin à une compilation si une classe spécifiée dans le fichier MOF existe déjà dans WMI.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="f6f1c-112">ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="f6f1c-112">forceupdate</span></span> | <span data-ttu-id="f6f1c-113">Force les mises à jour des classes lorsque des classes enfants sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="f6f1c-114">Par exemple, si vous définissez un qualificateur de classe dans une classe enfant et que la classe de base tente d’ajouter le même qualificateur, l’utilisation de cet indicateur force le compilateur à résoudre ce conflit en supprimant le qualificateur en conflit dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="f6f1c-115">Si la classe enfant a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="f6f1c-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="f6f1c-116">safeupdate</span></span>  | <span data-ttu-id="f6f1c-117">Permet au compilateur de mettre à jour des classes même si des classes enfants existent, si la modification ne provoque pas de conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="f6f1c-118">Par exemple, cet indicateur vous permet d’ajouter une nouvelle propriété à une classe de base sans avoir à ajouter la propriété à une classe enfant préexistante.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="f6f1c-119">Si les classes enfants ont des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="f6f1c-120">updateonly</span><span class="sxs-lookup"><span data-stu-id="f6f1c-120">updateonly</span></span>  | <span data-ttu-id="f6f1c-121">Indique au compilateur de ne pas créer de nouvelles classes et force le compilateur à arrêter la compilation si une classe spécifiée dans le fichier MOF n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="f6f1c-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="f6f1c-122">Examples</span></span>

<span data-ttu-id="f6f1c-123">L’exemple suivant montre comment utiliser cette commande avec les indicateurs updateonly et ForceUpdate.</span><span class="sxs-lookup"><span data-stu-id="f6f1c-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="f6f1c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6f1c-124">Requirements</span></span>



| <span data-ttu-id="f6f1c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6f1c-125">Requirement</span></span> | <span data-ttu-id="f6f1c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6f1c-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f6f1c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6f1c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f1c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6f1c-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f6f1c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6f1c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f1c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6f1c-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6f1c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6f1c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f1c-132">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="f6f1c-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




