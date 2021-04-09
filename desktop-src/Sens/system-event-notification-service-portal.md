---
description: Surveiller les notifications d’événements système à partir de programmes exécutés sur des ordinateurs portables pour déterminer la bande passante et la latence de la connexion réseau. Écrire des applications optimisées pour l’informatique mobile et les réseaux locaux à latence élevée.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Service de notification d’événements système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952695"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="2906c-104">Service de notification d’événements système</span><span class="sxs-lookup"><span data-stu-id="2906c-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="2906c-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="2906c-105">Purpose</span></span>

<span data-ttu-id="2906c-106">Les applications conçues pour être utilisées par les utilisateurs mobiles nécessitent un ensemble unique de fonctions de connectivité et de notifications.</span><span class="sxs-lookup"><span data-stu-id="2906c-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="2906c-107">Au passé, ces applications individuelles devaient implémenter ces fonctionnalités en interne.</span><span class="sxs-lookup"><span data-stu-id="2906c-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="2906c-108">Le service de notification d’événements système (SENS) fournit maintenant ces fonctionnalités dans le système d’exploitation, créant une interface de notification et de connectivité uniforme pour les applications.</span><span class="sxs-lookup"><span data-stu-id="2906c-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="2906c-109">L’utilisation de développeurs SENSe peut déterminer les informations de latence et de bande passante de connexion à partir de leur application et optimiser l’opération de l’application en fonction de ces conditions.</span><span class="sxs-lookup"><span data-stu-id="2906c-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2906c-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="2906c-110">Where applicable</span></span>

<span data-ttu-id="2906c-111">Les fonctions de connectivité et les notifications de SENS sont utiles pour les applications écrites pour des ordinateurs portables ou des ordinateurs connectés à des réseaux locaux à latence élevée.</span><span class="sxs-lookup"><span data-stu-id="2906c-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2906c-112">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="2906c-112">Developer audience</span></span>

<span data-ttu-id="2906c-113">Ce document est destiné aux développeurs de logiciels qui développent des applications pour l’informatique mobile et des réseaux locaux à latence élevée.</span><span class="sxs-lookup"><span data-stu-id="2906c-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="2906c-114">Ce document fournit une référence complète de toutes les parties du service de notification d’événements système, y compris l’objet SENS et les méthodes de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2906c-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2906c-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="2906c-115">Run-time requirements</span></span>

<span data-ttu-id="2906c-116">Nécessite Microsoft Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2906c-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="2906c-117">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une interface ou une fonction particulière, consultez la section Configuration requise de la documentation.</span><span class="sxs-lookup"><span data-stu-id="2906c-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2906c-118">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="2906c-118">In this section</span></span>



| <span data-ttu-id="2906c-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2906c-119">Topic</span></span>                                                              | <span data-ttu-id="2906c-120">Description</span><span class="sxs-lookup"><span data-stu-id="2906c-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="2906c-121">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="2906c-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="2906c-122">Informations générales sur le service de notification d’événements système.</span><span class="sxs-lookup"><span data-stu-id="2906c-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="2906c-123">Référence</span><span class="sxs-lookup"><span data-stu-id="2906c-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="2906c-124">Documentation des interfaces et méthodes du service de notification d’événements système.</span><span class="sxs-lookup"><span data-stu-id="2906c-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2906c-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2906c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2906c-126">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="2906c-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
