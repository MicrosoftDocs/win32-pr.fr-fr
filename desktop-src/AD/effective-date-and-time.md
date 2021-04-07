---
title: Date et heure d’effet
description: La date et l’heure effectives sont une stratégie d’évitement qui empêche les mises à jour partielles et de décalage de version en reportant les données d’informations effectives à un moment donné lorsque la modification a une probabilité élevée de réplication complète.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028626"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="737a1-103">Date et heure d’effet</span><span class="sxs-lookup"><span data-stu-id="737a1-103">Effective Date and Time</span></span>

<span data-ttu-id="737a1-104">La *date et l’heure effectives* sont une stratégie d’évitement qui empêche les mises à jour partielles et de décalage de version en reportant les données d’informations effectives à un moment donné lorsque la modification a une probabilité élevée de réplication complète.</span><span class="sxs-lookup"><span data-stu-id="737a1-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="737a1-105">Pour implémenter des dates d’effet, les objets d’application doivent inclure un horodatage de date d’effet, qui est rempli lorsque l’objet est créé ou modifié.</span><span class="sxs-lookup"><span data-stu-id="737a1-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="737a1-106">Les consommateurs des objets vérifient l’horodateur et retardent l’utilisation des objets jusqu’à ce que la date et l’heure soient atteintes.</span><span class="sxs-lookup"><span data-stu-id="737a1-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="737a1-107">Quelques points importants à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="737a1-107">Some important considerations:</span></span>

-   <span data-ttu-id="737a1-108">Les applications qui choisissent cette approche doivent s’assurer qu’il existe un ensemble de données applicables à utiliser jusqu’à ce que les objets mis à jour prennent effet.</span><span class="sxs-lookup"><span data-stu-id="737a1-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="737a1-109">Le service de temps distribué dans Windows NT 4,0 maintient la synchronisation des horloges de Windows 2000 connectées.</span><span class="sxs-lookup"><span data-stu-id="737a1-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="737a1-110">Toutefois, aucun service de temps n’est parfait. il y a donc une petite fenêtre pour le décalage de version.</span><span class="sxs-lookup"><span data-stu-id="737a1-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="737a1-111">La définition d’une date d’effet correcte suppose une connaissance de la latence globale de la réplication pour le système distribué en question.</span><span class="sxs-lookup"><span data-stu-id="737a1-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="737a1-112">Dans un réseau stable, une bonne règle empirique pour les dates d’effet est le (heure de la mise à jour) + (2 \* (latence globale moyenne)).</span><span class="sxs-lookup"><span data-stu-id="737a1-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="737a1-113">Ainsi, pour un système dont la latence totale est de 4 heures, un délai de 8 heures est raisonnable.</span><span class="sxs-lookup"><span data-stu-id="737a1-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="737a1-114">Dans un réseau instable, il est beaucoup plus difficile de déterminer une « bonne » valeur pour les dates d’effet, car la latence peut être fortement variable.</span><span class="sxs-lookup"><span data-stu-id="737a1-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="737a1-115">La date d’effet est plus « effective » dans un réseau instable lorsqu’elle est associée à d’autres stratégies d’évasion ou de détection, telles que des sommes de contrôle ou des GUID de cohérence.</span><span class="sxs-lookup"><span data-stu-id="737a1-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="737a1-116">Pour plus d’informations, consultez [checksums et nombre d’objets](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="737a1-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




