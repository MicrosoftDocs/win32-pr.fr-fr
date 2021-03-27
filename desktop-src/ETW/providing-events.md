---
description: Les fournisseurs sont des applications qui contiennent l’instrumentation de traçage d’événements.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Fournir des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972190"
---
# <a name="providing-events"></a><span data-ttu-id="d1658-103">Fournir des événements</span><span class="sxs-lookup"><span data-stu-id="d1658-103">Providing Events</span></span>

<span data-ttu-id="d1658-104">Les fournisseurs sont des applications qui contiennent l’instrumentation de traçage d’événements.</span><span class="sxs-lookup"><span data-stu-id="d1658-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="d1658-105">Une fois qu’un fournisseur s’est inscrit lui-même, un contrôleur peut ensuite activer ou désactiver le suivi des événements dans le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d1658-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="d1658-106">Le fournisseur définit son interprétation de l’activation ou de la désactivation.</span><span class="sxs-lookup"><span data-stu-id="d1658-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="d1658-107">En général, un fournisseur activé génère des événements, et un fournisseur désactivé ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="d1658-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="d1658-108">Cela vous permet d’ajouter le suivi d’événements à votre application sans qu’il ne soit nécessaire de générer des événements en permanence.</span><span class="sxs-lookup"><span data-stu-id="d1658-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="d1658-109">Cette section vous montre comment :</span><span class="sxs-lookup"><span data-stu-id="d1658-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="d1658-110">Événements d’écriture</span><span class="sxs-lookup"><span data-stu-id="d1658-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="d1658-111">Événements liés à l’écriture</span><span class="sxs-lookup"><span data-stu-id="d1658-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="d1658-112">Publier votre schéma d’événement à partager avec les consommateurs</span><span class="sxs-lookup"><span data-stu-id="d1658-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="d1658-113">Pour plus d’informations sur le contrôle des sessions de suivi d’événements, consultez [contrôle des sessions de suivi d’événements](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="d1658-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="d1658-114">Pour plus d’informations sur l’utilisation des événements à partir d’un fournisseur de suivi d’événements, consultez [consommation d’événements](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="d1658-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



