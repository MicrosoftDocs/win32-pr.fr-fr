---
description: Dérivation à partir de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Dérivation à partir de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515764"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="0ba98-103">Dérivation à partir de CBasePin</span><span class="sxs-lookup"><span data-stu-id="0ba98-103">Deriving from CBasePin</span></span>

<span data-ttu-id="0ba98-104">Pour implémenter un code confidentiel à l’aide de [**CBasePin**](cbasepin.md), vous devez dériver une nouvelle classe de la classe de base et substituer plusieurs de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="0ba98-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="0ba98-105">Vous devez substituer les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ba98-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="0ba98-106">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="0ba98-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="0ba98-107">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="0ba98-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="0ba98-108">Vous devrez probablement remplacer ces méthodes supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="0ba98-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="0ba98-109">**CBasePin :: actif**</span><span class="sxs-lookup"><span data-stu-id="0ba98-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="0ba98-110">**CBasePin::BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="0ba98-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="0ba98-111">**CBasePin::CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="0ba98-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="0ba98-112">**CBasePin::CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="0ba98-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="0ba98-113">**CBasePin :: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="0ba98-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="0ba98-114">**CBasePin :: inactif**</span><span class="sxs-lookup"><span data-stu-id="0ba98-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="0ba98-115">**CBasePin :: Notify**</span><span class="sxs-lookup"><span data-stu-id="0ba98-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="0ba98-116">**CBasePin :: Run**</span><span class="sxs-lookup"><span data-stu-id="0ba98-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="0ba98-117">Enfin, vous devez implémenter les méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="0ba98-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="0ba98-118">Certaines de ces méthodes sont implémentées dans les classes de base qui dérivent de **CBasePin**, telles que [**CBaseInputPin**](cbaseinputpin.md) et [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="0ba98-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ba98-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ba98-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ba98-120">**CBasePin**</span><span class="sxs-lookup"><span data-stu-id="0ba98-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



