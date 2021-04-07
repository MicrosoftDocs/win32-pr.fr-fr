---
description: Vue d’ensemble de la notification d’événement
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Vue d’ensemble de la notification d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746565"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="245a5-103">Vue d’ensemble de la notification d’événement</span><span class="sxs-lookup"><span data-stu-id="245a5-103">Overview of Event Notification</span></span>

<span data-ttu-id="245a5-104">Un filtre notifie le gestionnaire de graphique de filtre à propos d’un événement en publiant une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="245a5-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="245a5-105">L’événement peut être une opération attendue, comme la fin d’un flux de données, ou il peut représenter une erreur, telle qu’un échec de rendu d’un flux.</span><span class="sxs-lookup"><span data-stu-id="245a5-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="245a5-106">Le gestionnaire de graphes de filtre gère certains événements de filtre par lui-même, et laisse les autres éléments que l’application doit gérer.</span><span class="sxs-lookup"><span data-stu-id="245a5-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="245a5-107">Si le gestionnaire de graphique de filtre ne gère pas d’événement de filtre, il place la notification d’événement dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="245a5-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="245a5-108">Le graphique de filtre peut également en file d’attente ses propres notifications d’événements pour l’application.</span><span class="sxs-lookup"><span data-stu-id="245a5-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="245a5-109">Une application récupère les événements de la file d’attente et y répond en fonction du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="245a5-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="245a5-110">La notification d’événements dans DirectShow est donc similaire au schéma de mise en file d’attente de messages Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="245a5-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="245a5-111">Une application peut également annuler le comportement par défaut du gestionnaire de graphes de filtres pour un type d’événement donné.</span><span class="sxs-lookup"><span data-stu-id="245a5-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="245a5-112">Le gestionnaire de graphique de filtre place ensuite ces événements directement dans la file d’attente que l’application doit gérer.</span><span class="sxs-lookup"><span data-stu-id="245a5-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="245a5-113">Ce mécanisme active</span><span class="sxs-lookup"><span data-stu-id="245a5-113">This mechanism enables</span></span>

-   <span data-ttu-id="245a5-114">Gestionnaire de graphique de filtre pour communiquer avec l’application.</span><span class="sxs-lookup"><span data-stu-id="245a5-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="245a5-115">Filtres pour communiquer avec l’application et le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="245a5-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="245a5-116">L’application pour déterminer son degré d’implication dans la gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="245a5-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



