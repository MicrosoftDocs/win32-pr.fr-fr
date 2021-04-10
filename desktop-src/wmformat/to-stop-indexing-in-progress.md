---
title: Pour arrêter l’indexation en cours
description: Pour arrêter l’indexation en cours
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK, arrêt de l’indexation en cours
- ASF (Advanced Systems Format), arrêt de l’indexation en cours
- ASF (format avancé des systèmes), arrêt de l’indexation en cours
- index, arrêt de l’indexation en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030826"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="0c7c9-107">Pour arrêter l’indexation en cours</span><span class="sxs-lookup"><span data-stu-id="0c7c9-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="0c7c9-108">Une fois que vous avez commencé l’indexation à l’aide d’un appel à [**IWMIndexer :: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), l’indexeur continue normalement jusqu’à ce que le fichier soit indexé.</span><span class="sxs-lookup"><span data-stu-id="0c7c9-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="0c7c9-109">Vous pouvez arrêter les opérations d’indexation en appelant la méthode [**IWMIndexer :: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) .</span><span class="sxs-lookup"><span data-stu-id="0c7c9-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="0c7c9-110">Après avoir annulé l’indexation, vous pouvez appeler de nouveau **StartIndexing** , mais l’indexeur démarrera à partir du début du fichier au lieu de reprendre à partir du point d’annulation.</span><span class="sxs-lookup"><span data-stu-id="0c7c9-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="0c7c9-111">Étant donné que **StartIndexing** est un appel asynchrone, vous devrez normalement appeler **Cancel** à partir d’un autre thread ou gestionnaire d’événements dans votre application.</span><span class="sxs-lookup"><span data-stu-id="0c7c9-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="0c7c9-112">En général, **Cancel** est appelé à partir d’une procédure d’événement associée à un contrôle Button d’une application Windows.</span><span class="sxs-lookup"><span data-stu-id="0c7c9-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="0c7c9-113">Lorsque l’indexation est annulée, l’indexeur transmet un message d’état de WMT \_ Closed, comme si le fichier avait été indexé correctement.</span><span class="sxs-lookup"><span data-stu-id="0c7c9-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c7c9-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c7c9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c7c9-115">**Interface IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="0c7c9-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="0c7c9-116">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="0c7c9-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




