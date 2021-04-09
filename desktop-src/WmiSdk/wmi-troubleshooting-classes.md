---
description: WMI fournit un ensemble de classes de dépannage que les scripts et les applications peuvent utiliser pour obtenir des informations sur l’état interne de WMI pendant les opérations de fournisseur et de noyau WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classes de résolution des problèmes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953043"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="b0c87-103">Classes de résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="b0c87-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="b0c87-104">WMI fournit un ensemble de classes de dépannage que les scripts et les applications peuvent utiliser pour obtenir des informations sur l’état interne de WMI pendant les opérations de fournisseur et de noyau WMI.</span><span class="sxs-lookup"><span data-stu-id="b0c87-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="b0c87-105">Pour plus d’informations sur la résolution des problèmes liés à WMI, consultez [Dépannage WMI](wmi-troubleshooting.md) et [classes de dépannage et de](provider-configuration-and-troubleshooting-classes.md)résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b0c87-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="b0c87-106">WMI propose plusieurs classes de dépannage de base pour les opérations du fournisseur et du noyau WMI :</span><span class="sxs-lookup"><span data-stu-id="b0c87-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="b0c87-107">**\_Compteurs WMIPROVIDER \_ msft**</span><span class="sxs-lookup"><span data-stu-id="b0c87-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="b0c87-108">Seule une de ces classes est trouvée sur chaque système informatique.</span><span class="sxs-lookup"><span data-stu-id="b0c87-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="b0c87-109">Il fournit le nombre de différents types d’opérations de fournisseur sur ce système.</span><span class="sxs-lookup"><span data-stu-id="b0c87-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="b0c87-110">**\_WMISELFEVENT msft**</span><span class="sxs-lookup"><span data-stu-id="b0c87-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="b0c87-111">Les classes de dépannage d’événements dérivent de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span><span class="sxs-lookup"><span data-stu-id="b0c87-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="b0c87-112">Les requêtes de cette classe retournent des instances de classes d’événements telles que [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) ou [**msft \_ wmiprovider \_ CreateInstanceEnumAsyncEvent \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="b0c87-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="b0c87-113">La liste suivante fournit des liens vers différentes catégories de classes d’événements dérivées de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span><span class="sxs-lookup"><span data-stu-id="b0c87-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="b0c87-114">Classes de dépannage des événements du fournisseur</span><span class="sxs-lookup"><span data-stu-id="b0c87-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="b0c87-115">Classes de dépannage ConsumerProvider</span><span class="sxs-lookup"><span data-stu-id="b0c87-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="b0c87-116">Classes de dépannage des événements du service WMI</span><span class="sxs-lookup"><span data-stu-id="b0c87-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="b0c87-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0c87-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0c87-118">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="b0c87-118">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b0c87-119">Réception d’un événement WMI</span><span class="sxs-lookup"><span data-stu-id="b0c87-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
