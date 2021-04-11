---
description: Notification de la CBasePin des modifications d’état de filtre
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notification de la CBasePin des modifications d’état de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317677"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="536ab-103">Notification de la CBasePin des modifications d’état de filtre</span><span class="sxs-lookup"><span data-stu-id="536ab-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="536ab-104">La classe **CBasePin** est notifiée chaque fois que l’état du filtre propriétaire change.</span><span class="sxs-lookup"><span data-stu-id="536ab-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="536ab-105">Pour chaque transition d’État, le filtre appelle une méthode correspondante sur le code confidentiel, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="536ab-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="536ab-106">Nouvel état de filtre</span><span class="sxs-lookup"><span data-stu-id="536ab-106">New Filter State</span></span> | <span data-ttu-id="536ab-107">Méthode CBasePin</span><span class="sxs-lookup"><span data-stu-id="536ab-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="536ab-108">Arrêté</span><span class="sxs-lookup"><span data-stu-id="536ab-108">Stopped</span></span>          | [<span data-ttu-id="536ab-109">**CBasePin :: inactif**</span><span class="sxs-lookup"><span data-stu-id="536ab-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="536ab-110">Suspendu</span><span class="sxs-lookup"><span data-stu-id="536ab-110">Paused</span></span>           | [<span data-ttu-id="536ab-111">**CBasePin :: actif**</span><span class="sxs-lookup"><span data-stu-id="536ab-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="536ab-112">En cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="536ab-112">Running</span></span>          | [<span data-ttu-id="536ab-113">**CBasePin :: Run**</span><span class="sxs-lookup"><span data-stu-id="536ab-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="536ab-114">La classe dérivée doit substituer ces méthodes pour répondre au changement d’État.</span><span class="sxs-lookup"><span data-stu-id="536ab-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="536ab-115">Selon le filtre, le code pin peut démarrer un thread de travail qui remet les exemples, valide ou annule son allocateur de mémoire, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="536ab-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



