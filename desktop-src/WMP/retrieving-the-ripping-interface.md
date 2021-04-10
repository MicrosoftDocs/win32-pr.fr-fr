---
title: Récupération de l’interface d’extraction
description: Récupération de l’interface d’extraction
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, interface IWMPCdromRip
- extraction de CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103841962"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="05078-113">Récupération de l’interface d’extraction</span><span class="sxs-lookup"><span data-stu-id="05078-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="05078-114">Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="05078-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="05078-115">Récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="05078-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="05078-116">En utilisant les méthodes d' [extraction de \_ nombre](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) et d' [élément](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , vous pouvez effectuer une itération de la collection pour récupérer une interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) pour chaque lecteur de CD sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05078-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="05078-117">L’interface **IWMPCdrom** représente un lecteur de CD individuel.</span><span class="sxs-lookup"><span data-stu-id="05078-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="05078-118">Avant de commencer l’extraction d’un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer l’interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .</span><span class="sxs-lookup"><span data-stu-id="05078-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="05078-119">L’exemple de code suivant montre comment récupérer une interface pour extraire un CD d’un lecteur spécifique :</span><span class="sxs-lookup"><span data-stu-id="05078-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="05078-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05078-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05078-121">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="05078-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="05078-122">**Démarrage du processus RIP**</span><span class="sxs-lookup"><span data-stu-id="05078-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="05078-123">**Récupération de l’État RIP**</span><span class="sxs-lookup"><span data-stu-id="05078-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="05078-124">**Sélection d’éléments pour l’extraction**</span><span class="sxs-lookup"><span data-stu-id="05078-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="05078-125">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="05078-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




