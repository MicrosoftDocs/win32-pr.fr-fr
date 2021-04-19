---
description: La liste suivante contient les méthodes publiques CMSPCallMultiGraph appelées par le pool de threads.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: CMSPCallMultiGraph, méthodes publiques, appelées par le pool de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534529"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="9561e-103">CMSPCallMultiGraph, méthodes publiques, appelées par le pool de threads</span><span class="sxs-lookup"><span data-stu-id="9561e-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="9561e-104">Méthodes publiques CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="9561e-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="9561e-105">Description</span><span class="sxs-lookup"><span data-stu-id="9561e-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9561e-106">**DispatchGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="9561e-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="9561e-107">Appelé lorsque le graphique de filtre signale un événement.</span><span class="sxs-lookup"><span data-stu-id="9561e-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="9561e-108">**HandleGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="9561e-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="9561e-109">Appelée par la méthode statique [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) .</span><span class="sxs-lookup"><span data-stu-id="9561e-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="9561e-110">Met en file d’attente [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) sur le thread de travail MSP principal.</span><span class="sxs-lookup"><span data-stu-id="9561e-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="9561e-111">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="9561e-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="9561e-112">Autorise l’instance de l’objet d’appel MSP à gérer l’événement du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9561e-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9561e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9561e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9561e-114">**CMSPCallMultiGraph**</span><span class="sxs-lookup"><span data-stu-id="9561e-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



