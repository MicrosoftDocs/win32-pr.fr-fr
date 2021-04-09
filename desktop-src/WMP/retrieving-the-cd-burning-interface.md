---
title: Récupération de l’interface de gravure de CD
description: Récupération de l’interface de gravure de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, récupération de l’interface IWMPCdromCollection
- gravure de CD, récupération de l’interface IWMPCdromCollection
- Interface IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030921"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="339b4-113">Récupération de l’interface de gravure de CD</span><span class="sxs-lookup"><span data-stu-id="339b4-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="339b4-114">Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="339b4-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="339b4-115">Vous récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="339b4-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="339b4-116">En utilisant les méthodes d' **extraction de \_ nombre** et d' **élément** , vous pouvez effectuer une itération de la collection pour récupérer un pointeur d’interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) pour chaque lecteur de CD sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="339b4-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="339b4-117">L’interface **IWMPCdrom** représente un lecteur de CD individuel.</span><span class="sxs-lookup"><span data-stu-id="339b4-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="339b4-118">Avant de commencer à graver un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer un pointeur vers l’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .</span><span class="sxs-lookup"><span data-stu-id="339b4-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="339b4-119">L’exemple de code suivant montre comment récupérer une interface pour la gravure d’un CD sur un lecteur spécifique :</span><span class="sxs-lookup"><span data-stu-id="339b4-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="339b4-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="339b4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="339b4-121">**Gravure d’un CD**</span><span class="sxs-lookup"><span data-stu-id="339b4-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="339b4-122">**Démarrage du processus de gravure**</span><span class="sxs-lookup"><span data-stu-id="339b4-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="339b4-123">**Effacement d’un CD réinscriptible**</span><span class="sxs-lookup"><span data-stu-id="339b4-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="339b4-124">**Récupération de l’état du lecteur et du disque**</span><span class="sxs-lookup"><span data-stu-id="339b4-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="339b4-125">**Récupération de l’état d’avancement**</span><span class="sxs-lookup"><span data-stu-id="339b4-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="339b4-126">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="339b4-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




