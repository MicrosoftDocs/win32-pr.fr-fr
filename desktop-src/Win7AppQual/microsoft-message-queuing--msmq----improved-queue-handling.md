---
description: Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088157"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="f9918-103">Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente</span><span class="sxs-lookup"><span data-stu-id="f9918-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="f9918-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="f9918-104">Platforms</span></span>

<span data-ttu-id="f9918-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9918-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="f9918-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9918-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="f9918-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f9918-107">Feature Impact</span></span>

 <span data-ttu-id="f9918-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="f9918-108">**Severity** - Low</span></span>  
<span data-ttu-id="f9918-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="f9918-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="f9918-110">Description</span><span class="sxs-lookup"><span data-stu-id="f9918-110">Description</span></span>

<span data-ttu-id="f9918-111">Le service MSMQ n’a pas de limite matérielle sur le nombre de files d’attente qui peuvent être créées sur un système.</span><span class="sxs-lookup"><span data-stu-id="f9918-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="f9918-112">Toutefois, les performances du système sont affectées lors de la création d’un grand nombre de files d’attente.</span><span class="sxs-lookup"><span data-stu-id="f9918-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="f9918-113">Plus précisément, lorsqu’il y a plus de quelques milliers de files d’attente, le temps de démarrage du service MSMQ augmente de façon exponentielle, ce qui a un impact visible.</span><span class="sxs-lookup"><span data-stu-id="f9918-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="f9918-114">Microsoft a optimisé le démarrage du service MSMQ dans Windows 7 afin de réduire la surcharge de recherche pour le chargement des files d’attente en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f9918-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="f9918-115">Cette optimisation a entraîné une amélioration spectaculaire du temps de démarrage du service MSMQ, même lorsque plusieurs milliers de files d’attente sont créées dans le système.</span><span class="sxs-lookup"><span data-stu-id="f9918-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f9918-116">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="f9918-116">Manifestation of Impact</span></span>

<span data-ttu-id="f9918-117">Cette amélioration des performances n’a pas d’impact sur les fonctionnalités d’une application existante.</span><span class="sxs-lookup"><span data-stu-id="f9918-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="f9918-118">Tirer parti de la fonctionnalité modifiée</span><span class="sxs-lookup"><span data-stu-id="f9918-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="f9918-119">Les développeurs d’applications utilisant MSMQ sur Windows 7 peuvent désormais concevoir leurs solutions sans limiter le nombre de files d’attente.</span><span class="sxs-lookup"><span data-stu-id="f9918-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="f9918-120">Notez que le nombre de files d’attente affecte toujours les performances globales du serveur MSMQ, mais l’impact sur les performances est désormais linéaire au lieu d’une mise à l’échelle exponentielle.</span><span class="sxs-lookup"><span data-stu-id="f9918-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="f9918-121">Compatibilité, performances, fiabilité et tests d’utilisation</span><span class="sxs-lookup"><span data-stu-id="f9918-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="f9918-122">Si vous utilisez un grand nombre de files d’attente, Simulez l’environnement de production sur un banc d’essai, surveillez les performances et analysez le temps de démarrage du service et le débit des messages avec un grand nombre de files d’attente et de messages présents dans le système de test.</span><span class="sxs-lookup"><span data-stu-id="f9918-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



