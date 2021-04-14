---
title: À propos des services Web Windows
description: L’API des services Web Windows est une API en couches et peut être illustrée comme suit.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104568695"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="395bb-103">À propos des services Web Windows</span><span class="sxs-lookup"><span data-stu-id="395bb-103">About Windows Web Services</span></span>

<span data-ttu-id="395bb-104">L’API des services Web Windows est une API en couches et peut être illustrée comme suit</span><span class="sxs-lookup"><span data-stu-id="395bb-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Diagramme montrant les couches et les zones inter-couches de l’API des services Web Windows.](images/apistack.png)

<span data-ttu-id="395bb-106">Le WWSAPI est une API en couches.</span><span class="sxs-lookup"><span data-stu-id="395bb-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="395bb-107">Nous pensons que la plupart des développeurs ciblent le modèle de service, qui est un modèle de programmation basé sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="395bb-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="395bb-108">Dans le modèle de service, l’hôte de service fournit le modèle de programmation côté serveur, tandis que le proxy de service fournit le modèle de programmation côté client.</span><span class="sxs-lookup"><span data-stu-id="395bb-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="395bb-109">Chaque couche expose un ensemble d’API et de types qui peuvent être utilisés avec les API de cette couche.</span><span class="sxs-lookup"><span data-stu-id="395bb-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="395bb-110">Modèle de service</span><span class="sxs-lookup"><span data-stu-id="395bb-110">Service Model</span></span>

<span data-ttu-id="395bb-111">La couche de niveau supérieur appelée le [modèle de service](service-model-layer-overview.md) fournit un modèle de programmation basé sur une méthode qui est le modèle le plus simple à utiliser.</span><span class="sxs-lookup"><span data-stu-id="395bb-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="395bb-112">Dans le modèle de service, l' [hôte de service](service-host.md) fournit le modèle de programmation côté serveur, tandis que le proxy de [service](service-proxy.md) fournit le modèle de programmation côté client.</span><span class="sxs-lookup"><span data-stu-id="395bb-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="395bb-113">Le [contexte](context.md) est utilisé dans le modèle de service pour passer un État pertinent à la disposition de l’opération de service et/ou du rappel lorsqu’il est appelé.</span><span class="sxs-lookup"><span data-stu-id="395bb-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="395bb-114">Le [contrat de service](contract.md) est utilisé pour spécifier un contrat de service sur un point de terminaison exposé sur le service.</span><span class="sxs-lookup"><span data-stu-id="395bb-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="395bb-115">Les composants et opérations suivants font partie de la couche de service :</span><span class="sxs-lookup"><span data-stu-id="395bb-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="395bb-116">Hôte de service</span><span class="sxs-lookup"><span data-stu-id="395bb-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="395bb-117">Proxy de service</span><span class="sxs-lookup"><span data-stu-id="395bb-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="395bb-118">Contexte</span><span class="sxs-lookup"><span data-stu-id="395bb-118">Context</span></span>](context.md)
-   [<span data-ttu-id="395bb-119">Façon</span><span class="sxs-lookup"><span data-stu-id="395bb-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="395bb-120">Métadonnées du service</span><span class="sxs-lookup"><span data-stu-id="395bb-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="395bb-121">Couche de canal</span><span class="sxs-lookup"><span data-stu-id="395bb-121">Channel Layer</span></span>

<span data-ttu-id="395bb-122">Le modèle de service repose sur une couche de canal, ce qui offre une flexibilité totale, mais est plus difficile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="395bb-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="395bb-123">Les composants et opérations suivants font partie de la couche de canal :</span><span class="sxs-lookup"><span data-stu-id="395bb-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="395bb-124">Message</span><span class="sxs-lookup"><span data-stu-id="395bb-124">Message</span></span>](message.md)
-   [<span data-ttu-id="395bb-125">Channel</span><span class="sxs-lookup"><span data-stu-id="395bb-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="395bb-126">Port d'écoute</span><span class="sxs-lookup"><span data-stu-id="395bb-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="395bb-127">Erreurs</span><span class="sxs-lookup"><span data-stu-id="395bb-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="395bb-128">Url</span><span class="sxs-lookup"><span data-stu-id="395bb-128">Url</span></span>](url.md)
-   [<span data-ttu-id="395bb-129">Sécurité</span><span class="sxs-lookup"><span data-stu-id="395bb-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="395bb-130">Importation de métadonnées</span><span class="sxs-lookup"><span data-stu-id="395bb-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="395bb-131">Couche XML</span><span class="sxs-lookup"><span data-stu-id="395bb-131">XML Layer</span></span>

<span data-ttu-id="395bb-132">La couche de canal est à son tour basée sur une infrastructure XML légère, qui comprend la désérialisation des types de données C.</span><span class="sxs-lookup"><span data-stu-id="395bb-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="395bb-133">Les composants et opérations suivants font partie de la couche XML :</span><span class="sxs-lookup"><span data-stu-id="395bb-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="395bb-134">Enregistreur XML</span><span class="sxs-lookup"><span data-stu-id="395bb-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="395bb-135">Lecteur XML</span><span class="sxs-lookup"><span data-stu-id="395bb-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="395bb-136">Mémoire tampon XML</span><span class="sxs-lookup"><span data-stu-id="395bb-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="395bb-137">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="395bb-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="395bb-138">Prise en charge du langage XML</span><span class="sxs-lookup"><span data-stu-id="395bb-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="395bb-139">Commun à toutes les couches</span><span class="sxs-lookup"><span data-stu-id="395bb-139">Common to all layers</span></span>

<span data-ttu-id="395bb-140">Les rubriques suivantes s’appliquent à l’une des trois couches :</span><span class="sxs-lookup"><span data-stu-id="395bb-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="395bb-141">Erreurs</span><span class="sxs-lookup"><span data-stu-id="395bb-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="395bb-142">Modèle asynchrone</span><span class="sxs-lookup"><span data-stu-id="395bb-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="395bb-143">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="395bb-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="395bb-144">Suivi</span><span class="sxs-lookup"><span data-stu-id="395bb-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="395bb-145">Annulation</span><span class="sxs-lookup"><span data-stu-id="395bb-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="395bb-146">Utilitaires</span><span class="sxs-lookup"><span data-stu-id="395bb-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="395bb-147">Débogage</span><span class="sxs-lookup"><span data-stu-id="395bb-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="395bb-148">Outil compilateur Wsutil</span><span class="sxs-lookup"><span data-stu-id="395bb-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="395bb-149">Système</span><span class="sxs-lookup"><span data-stu-id="395bb-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="395bb-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="395bb-150">Examples</span></span>

<span data-ttu-id="395bb-151">Pour plus d’informations sur les éléments d’API, consultez [référence des services Web Windows](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="395bb-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="395bb-152">Pour obtenir des exemples d’utilisation de l’API, consultez [utilisation des services Web Windows](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="395bb-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




