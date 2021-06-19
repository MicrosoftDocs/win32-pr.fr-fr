---
description: Découvrez comment récupérer des données d’événement lorsque vous utilisez des événements. Pour utiliser des données spécifiques à un événement, le consommateur doit connaître le format des données d’événement.
ms.assetid: d783ff64-73c5-4ace-a866-38a42db7c8b6
title: Récupération de données d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477c79850a2325cea5c1a2536609e059b7cdab0b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394994"
---
# <a name="retrieving-event-data"></a><span data-ttu-id="50a4d-104">Récupération de données d’événement</span><span class="sxs-lookup"><span data-stu-id="50a4d-104">Retrieving Event Data</span></span>

<span data-ttu-id="50a4d-105">Pour utiliser des données spécifiques à un événement, le consommateur doit connaître le format des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="50a4d-105">To consume event specific data, the consumer must know the format of the event data.</span></span> <span data-ttu-id="50a4d-106">Ce n’est pas un problème si vous utilisez des événements de votre propre fournisseur, car vous connaissez le format des données.</span><span class="sxs-lookup"><span data-stu-id="50a4d-106">This is not an issue if you are consuming events from your own provider because you know the format of the data.</span></span> <span data-ttu-id="50a4d-107">Toutefois, pour utiliser un événement à partir de n’importe quel fournisseur, le fournisseur doit publier la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="50a4d-107">However, to consume an event from any provider, the provider must publish the layout of the event data.</span></span> <span data-ttu-id="50a4d-108">Pour obtenir une vue d’ensemble de la façon dont les métadonnées d’événement fonctionnent, ainsi que sur la façon de publier vos métadonnées d’événement afin que d’autres personnes puissent l’utiliser, consultez [vue d’ensemble des métadonnées](event-metadata-overview.md)</span><span class="sxs-lookup"><span data-stu-id="50a4d-108">For an overview of how event metadata operates as well as how to publish your event metadata so others can use it, see [Event Metadata Overview](event-metadata-overview.md).</span></span>

<span data-ttu-id="50a4d-109">Pour consommer des événements sur Windows Vista qui ont été publiés à l’aide d’un manifeste, de fichiers MOF ou TMF, ainsi que des événements TraceLogging, consultez [extraction de données d’événement à l’aide de Tdh](retrieving-event-data-using-tdh.md).</span><span class="sxs-lookup"><span data-stu-id="50a4d-109">To consume events on Windows Vista that were published using a manifest, MOF, or TMF files, as well as TraceLogging events, see [Retrieving Event Data Using TDH](retrieving-event-data-using-tdh.md).</span></span>

<span data-ttu-id="50a4d-110">Pour utiliser les événements antérieurs à Windows Vista qui ont été publiés à l’aide de MOF, consultez [extraction de données d’événement à l’aide de MOF](retrieving-event-data-using-mof.md).</span><span class="sxs-lookup"><span data-stu-id="50a4d-110">To consume events prior to Windows Vista that were published using MOF, see [Retrieving Event Data Using MOF](retrieving-event-data-using-mof.md).</span></span>

 

 



