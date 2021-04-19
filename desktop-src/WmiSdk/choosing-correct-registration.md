---
description: WMI prend en charge différents modèles de thread, selon la façon dont le fournisseur est hébergé et le type de fonctionnalité de fournisseur, tel que la classe ou la propriété.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Choix de l’inscription correcte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533926"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="59747-103">Choix de l’inscription correcte</span><span class="sxs-lookup"><span data-stu-id="59747-103">Choosing Correct Registration</span></span>

<span data-ttu-id="59747-104">WMI prend en charge différents modèles de thread, selon la façon dont le fournisseur est hébergé et le type de fonctionnalité de fournisseur, tel que la [classe](writing-a-class-provider.md) ou la [propriété](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="59747-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="59747-105">Par exemple, les [*fournisseurs découplés*](gloss-d.md) ne prennent pas en charge tous les types de fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="59747-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="59747-106">Pour plus d’informations sur les différents modèles d’hébergement et sur la façon de les configurer, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="59747-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="59747-107">Fournisseurs de In-Process</span><span class="sxs-lookup"><span data-stu-id="59747-107">In-Process Providers</span></span>

<span data-ttu-id="59747-108">Les fournisseurs in-process s’exécutent dans un processus hôte partagé, Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="59747-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="59747-109">La plupart des types de fournisseurs in-process utilisent le modèle de cloisonnement multithread (MTA).</span><span class="sxs-lookup"><span data-stu-id="59747-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="59747-110">Le modèle MTA est pris en charge pour les types de fonctionnalités de fournisseur suivants :</span><span class="sxs-lookup"><span data-stu-id="59747-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="59747-111">Fournisseur de classes</span><span class="sxs-lookup"><span data-stu-id="59747-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="59747-112">Fournisseur d’instance</span><span class="sxs-lookup"><span data-stu-id="59747-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="59747-113">Fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="59747-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="59747-114">Fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="59747-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="59747-115">Fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="59747-116">Fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="59747-117">Le modèle STA (Single-Threaded Apartment) est pris en charge pour certains types de fonctionnalités du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="59747-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="59747-118">Fournisseur d’instance</span><span class="sxs-lookup"><span data-stu-id="59747-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="59747-119">Fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="59747-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="59747-120">Fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="59747-121">Fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="59747-122">Fournisseurs hors processus</span><span class="sxs-lookup"><span data-stu-id="59747-122">Out-of-Process Providers</span></span>

<span data-ttu-id="59747-123">Les fournisseurs qui sont hébergés dans un autre hôte de service partagé prennent en charge la fonctionnalité de fournisseur suivante :</span><span class="sxs-lookup"><span data-stu-id="59747-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="59747-124">Fournisseur de classes</span><span class="sxs-lookup"><span data-stu-id="59747-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="59747-125">Fournisseur d’instance</span><span class="sxs-lookup"><span data-stu-id="59747-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="59747-126">Fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="59747-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="59747-127">Fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="59747-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="59747-128">Fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="59747-129">Fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="59747-130">Pour plus d’informations sur les hôtes de service partagés, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="59747-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="59747-131">Fournisseurs découplés</span><span class="sxs-lookup"><span data-stu-id="59747-131">Decoupled Providers</span></span>

<span data-ttu-id="59747-132">Les fournisseurs découplés sont hébergés dans une application.</span><span class="sxs-lookup"><span data-stu-id="59747-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="59747-133">Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="59747-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="59747-134">Les fournisseurs créés à l’aide de WMI dans le .NET Framework sont découplés.</span><span class="sxs-lookup"><span data-stu-id="59747-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="59747-135">Les fournisseurs découplés prennent en charge la fonctionnalité de fournisseur suivante :</span><span class="sxs-lookup"><span data-stu-id="59747-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="59747-136">Fournisseur d’instance</span><span class="sxs-lookup"><span data-stu-id="59747-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="59747-137">Fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="59747-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="59747-138">Fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="59747-139">Fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="59747-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="59747-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59747-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59747-141">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="59747-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="59747-142">Hébergement et sécurité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="59747-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



