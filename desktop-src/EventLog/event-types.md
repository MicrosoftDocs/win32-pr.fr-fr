---
description: Il existe cinq types d’événements qui peuvent être journalisés. Toutes ces données comportent des données communes bien définies et peuvent éventuellement inclure des données spécifiques à l’événement.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Types d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864245"
---
# <a name="event-types"></a><span data-ttu-id="6a784-104">Types d’événements</span><span class="sxs-lookup"><span data-stu-id="6a784-104">Event Types</span></span>

<span data-ttu-id="6a784-105">Il existe cinq types d’événements qui peuvent être journalisés.</span><span class="sxs-lookup"><span data-stu-id="6a784-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="6a784-106">Toutes ces données comportent des données communes bien définies et peuvent éventuellement inclure des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a784-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="6a784-107">L’application indique le type d’événement lorsqu’il signale un événement.</span><span class="sxs-lookup"><span data-stu-id="6a784-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="6a784-108">Chaque événement doit être d’un type unique.</span><span class="sxs-lookup"><span data-stu-id="6a784-108">Each event must be of a single type.</span></span> <span data-ttu-id="6a784-109">L’observateur d’événements affiche une icône différente pour chaque type dans le mode liste du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="6a784-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="6a784-110">Le tableau suivant décrit les cinq types d’événements utilisés dans la journalisation des événements.</span><span class="sxs-lookup"><span data-stu-id="6a784-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="6a784-111">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="6a784-111">Event type</span></span>        | <span data-ttu-id="6a784-112">Description</span><span class="sxs-lookup"><span data-stu-id="6a784-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a784-113">**Error**</span><span class="sxs-lookup"><span data-stu-id="6a784-113">**Error**</span></span>         | <span data-ttu-id="6a784-114">Événement qui indique un problème grave tel qu’une perte de données ou une perte de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6a784-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="6a784-115">Par exemple, si un service ne parvient pas à se charger au démarrage, un événement d’erreur est consigné.</span><span class="sxs-lookup"><span data-stu-id="6a784-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="6a784-116">**Avertissement**</span><span class="sxs-lookup"><span data-stu-id="6a784-116">**Warning**</span></span>       | <span data-ttu-id="6a784-117">Événement qui n’est pas nécessairement significatif, mais qui peut indiquer un éventuel problème futur.</span><span class="sxs-lookup"><span data-stu-id="6a784-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="6a784-118">Par exemple, lorsque l’espace disque est faible, un événement d’avertissement est enregistré.</span><span class="sxs-lookup"><span data-stu-id="6a784-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="6a784-119">Si une application peut effectuer une récupération à partir d’un événement sans perte de fonctionnalités ou de données, elle peut généralement classer l’événement comme un événement d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6a784-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="6a784-120">**Informations**</span><span class="sxs-lookup"><span data-stu-id="6a784-120">**Information**</span></span>   | <span data-ttu-id="6a784-121">Événement qui décrit la réussite de l’opération d’une application, d’un pilote ou d’un service.</span><span class="sxs-lookup"><span data-stu-id="6a784-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="6a784-122">Par exemple, lorsqu’un pilote réseau est chargé avec succès, il peut être approprié d’enregistrer un événement d’information.</span><span class="sxs-lookup"><span data-stu-id="6a784-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="6a784-123">Notez qu’il n’est généralement pas approprié pour une application de bureau de consigner un événement à chaque fois qu’elle démarre.</span><span class="sxs-lookup"><span data-stu-id="6a784-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="6a784-124">**Audit des succès**</span><span class="sxs-lookup"><span data-stu-id="6a784-124">**Success Audit**</span></span> | <span data-ttu-id="6a784-125">Événement qui enregistre une tentative d’accès de sécurité auditée réussie.</span><span class="sxs-lookup"><span data-stu-id="6a784-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="6a784-126">Par exemple, la tentative réussie d’un utilisateur pour se connecter au système est consignée comme un événement d’audit de réussite.</span><span class="sxs-lookup"><span data-stu-id="6a784-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="6a784-127">**Audit des échecs**</span><span class="sxs-lookup"><span data-stu-id="6a784-127">**Failure Audit**</span></span> | <span data-ttu-id="6a784-128">Événement qui enregistre une tentative d’accès de sécurité auditée qui échoue.</span><span class="sxs-lookup"><span data-stu-id="6a784-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="6a784-129">Par exemple, si un utilisateur tente d’accéder à un lecteur réseau et échoue, la tentative est consignée comme un événement d’audit d’échec.</span><span class="sxs-lookup"><span data-stu-id="6a784-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="6a784-130">Les activités sélectionnées des utilisateurs peuvent être suivies en auditant les événements de sécurité, puis en plaçant des entrées dans le journal de sécurité d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6a784-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



