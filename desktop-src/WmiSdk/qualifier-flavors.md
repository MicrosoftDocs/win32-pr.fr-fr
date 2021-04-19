---
description: Les types de qualificateurs fournissent des informations supplémentaires sur un qualificateur, par exemple si une classe ou une instance dérivée peut substituer la valeur d’origine des qualificateurs.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Types de qualificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538171"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="ffc0e-103">Types de qualificateurs</span><span class="sxs-lookup"><span data-stu-id="ffc0e-103">Qualifier Flavors</span></span>

<span data-ttu-id="ffc0e-104">Les versions de qualificateur fournissent des informations supplémentaires sur un qualificateur, par exemple si une classe ou une instance dérivée peut substituer la valeur d’origine du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="ffc0e-105">Les versions de qualificateur peuvent être ajoutées au début du fichier MOF, à l’aide de la syntaxe suivante, en provoquant leur application dans la définition.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="ffc0e-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ffc0e-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="ffc0e-107">Le **ToSubClass** et les versions **modifiées** s’appliquent à tous les qualificateurs de **Description** dans le MOF.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="ffc0e-108">Le tableau suivant répertorie les versions de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="ffc0e-109">Version du qualificateur</span><span class="sxs-lookup"><span data-stu-id="ffc0e-109">Qualifier Flavor</span></span>    | <span data-ttu-id="ffc0e-110">Signification</span><span class="sxs-lookup"><span data-stu-id="ffc0e-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc0e-111">**Modifiées**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-111">**Amended**</span></span>         | <span data-ttu-id="ffc0e-112">Le qualificateur n’est pas requis dans la définition de classe de base et peut être transféré à l’avenant à localiser.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="ffc0e-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-113">**DisableOverride**</span></span> | <span data-ttu-id="ffc0e-114">Le qualificateur ne peut pas être écrasé dans une classe ou une instance dérivée.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="ffc0e-115">Notez que la possibilité d’écraser un qualificateur propagé est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="ffc0e-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-116">**EnableOverride**</span></span>  | <span data-ttu-id="ffc0e-117">En cas de propagation vers une classe ou une instance dérivée, la valeur du qualificateur peut être substituée.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="ffc0e-118">La définition de **EnableOverride** est facultative, car la possibilité de remplacer la valeur de qualificateur est la fonctionnalité par défaut pour les qualificateurs propagés.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="ffc0e-119">**NotToInstance**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-119">**NotToInstance**</span></span>   | <span data-ttu-id="ffc0e-120">Le qualificateur n’est pas propagé aux instances de classe.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="ffc0e-121">**NotToSubClass**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-121">**NotToSubClass**</span></span>   | <span data-ttu-id="ffc0e-122">Le qualificateur n’est pas propagé aux classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="ffc0e-123">**Restreint**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-123">**Restricted**</span></span>      | <span data-ttu-id="ffc0e-124">Le qualificateur n’est pas propagé aux instances ou aux classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="ffc0e-125">**ToInstance**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-125">**ToInstance**</span></span>      | <span data-ttu-id="ffc0e-126">Le qualificateur est propagé aux instances.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ffc0e-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="ffc0e-127">**ToSubClass**</span></span>      | <span data-ttu-id="ffc0e-128">Le qualificateur est propagé aux classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="ffc0e-129">Cette version est uniquement appropriée pour les qualificateurs définis pour une classe et ne peut pas être attachée à un qualificateur décrivant une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="ffc0e-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



