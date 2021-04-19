---
description: Résumé du thread de filtre
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Résumé du thread de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530770"
---
# <a name="summary-of-filter-threading"></a><span data-ttu-id="727f3-103">Résumé du thread de filtre</span><span class="sxs-lookup"><span data-stu-id="727f3-103">Summary of Filter Threading</span></span>

<span data-ttu-id="727f3-104">Les méthodes suivantes sont appelées sur le thread de diffusion en continu :</span><span class="sxs-lookup"><span data-stu-id="727f3-104">The following methods are called on the streaming thread:</span></span>

-   [<span data-ttu-id="727f3-105">**IMemInputPin :: Receive**</span><span class="sxs-lookup"><span data-stu-id="727f3-105">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="727f3-106">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="727f3-106">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="727f3-107">**IPin :: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="727f3-107">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="727f3-108">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="727f3-108">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [<span data-ttu-id="727f3-109">**IMemAllocator :: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="727f3-109">**IMemAllocator::GetBuffer**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

<span data-ttu-id="727f3-110">Les méthodes suivantes sont appelées sur le thread d’application :</span><span class="sxs-lookup"><span data-stu-id="727f3-110">The following methods are called on the application thread:</span></span>

-   <span data-ttu-id="727f3-111">Changements d’État : [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span><span class="sxs-lookup"><span data-stu-id="727f3-111">State changes: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span></span>
-   <span data-ttu-id="727f3-112">Horloge de référence : [**IMediaFilter :: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span><span class="sxs-lookup"><span data-stu-id="727f3-112">Reference clock: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span></span>
-   <span data-ttu-id="727f3-113">Opérations de code confidentiel : [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span><span class="sxs-lookup"><span data-stu-id="727f3-113">Pin operations: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span></span>
-   <span data-ttu-id="727f3-114">Fonctions Allocator : [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span><span class="sxs-lookup"><span data-stu-id="727f3-114">Allocator functions: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span></span>
-   <span data-ttu-id="727f3-115">Vidage : [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="727f3-115">Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>

<span data-ttu-id="727f3-116">Cette liste n’est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="727f3-116">This list is not exhaustive.</span></span> <span data-ttu-id="727f3-117">Lorsque vous implémentez un filtre, vous devez prendre en compte les méthodes qui modifient l’état de filtre et les méthodes qui effectuent des opérations de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="727f3-117">When you implement a filter, you must consider which methods change the filter state, and which methods perform streaming operations.</span></span>

 

 



